project(
    'lincity-ng',
    'cpp',
    default_options: [
        'cpp_std=c++17',
    ],
)

compiler = meson.get_compiler('cpp')

if compiler.get_id() == 'gcc'
  extra_args = ['-lstdc++fs']
else
  extra_args = []
endif

conf_data = configuration_data()
conf_data.set('appdatadir', join_paths(get_option('prefix'), 'share'))
conf_data.set('package_name', 'LinCity-NG')
conf_data.set('package_version', '2.9')
configure_file(input : 'config_meson.h.in',
               output : 'config.h',
               configuration : conf_data)

physfs = compiler.find_library('physfs')
sdl = dependency('sdl')

physfsstream = shared_library(
    'physfsstream',
    [
        'src/PhysfsStream/PhysfsSDL.cpp',
        'src/PhysfsStream/PhysfsStream.cpp',
    ],
    include_directories: [
        include_directories('src'),
    ],
    dependencies: [
        physfs,
        sdl,
    ],
)

tinygettext = shared_library(
    'tinygettext',
    [
        'src/tinygettext/findlocale.cpp',
        'src/tinygettext/tinygettext.cpp',
    ],
    include_directories: [
        include_directories('src'),
    ],
    dependencies: [
        physfs,
        dependency('sdl'),
    ],
    link_with: [
        physfsstream,
    ],
)

executable(
    'lincity-ng',
    [
        'src/gui/Gradient.cpp',
        'src/gui/Component.cpp',
        'src/gui/DocumentImage.cpp',
        'src/gui/Rect2D.cpp',
        'src/gui/PainterGL/PainterGL.cpp',
        'src/gui/PainterGL/TextureManagerGL.cpp',
        'src/gui/PainterGL/TextureGL.cpp',
        'src/gui/TooltipManager.cpp',
        'src/gui/ScrollBar.cpp',
        'src/gui/Image.cpp',
        'src/gui/ScrollView.cpp',
        'src/gui/Desktop.cpp',
        'src/gui/Paragraph.cpp',
        'src/gui/TextureManager.cpp',
        'src/gui/FontManager.cpp',
        'src/gui/Style.cpp',
        'src/gui/Event.cpp',
        'src/gui/PainterSDL/TextureSDL.cpp',
        'src/gui/PainterSDL/PainterSDL.cpp',
        'src/gui/PainterSDL/TextureManagerSDL.cpp',
        'src/gui/ComponentFactory.cpp',
        'src/gui/Filter.cpp',
        'src/gui/ComponentLoader.cpp',
        'src/gui/Color.cpp',
        'src/gui/TableLayout.cpp',
        'src/gui/Document.cpp',
        'src/gui/Panel.cpp',
        'src/gui/XmlReader.cpp',
        'src/gui/Button.cpp',
        'src/gui/Window.cpp',
        'src/gui/SwitchComponent.cpp',
        'src/gui/Child.cpp',
        'src/gui/FilledRectangle.cpp',

        'src/lincity/lclib.cpp',
        'src/lincity/stats.cpp',
        'src/lincity/world.cpp',
        'src/lincity/engine.cpp',
        'src/lincity/engglobs.cpp',
        'src/lincity/fileutil.cpp',
        'src/lincity/lintypes.cpp',
        'src/lincity/loadsave.cpp',
        'src/lincity/simulate.cpp',
        'src/lincity/Vehicles.cpp',
        'src/lincity/init_game.cpp',
        'src/lincity/lc_locale.cpp',
        'src/lincity/transport.cpp',
        'src/lincity/xmlloadsave.cpp',
        'src/lincity/old_ldsvguts.cpp',
        'src/lincity/all_buildings.cpp',
        'src/lincity/UserOperation.cpp',
        'src/lincity/ConstructionCount.cpp',
        'src/lincity/ConstructionManager.cpp',
        'src/lincity/ConstructionRequest.cpp',
        'src/lincity/modules/tip.cpp',
        'src/lincity/modules/fire.cpp',
        'src/lincity/modules/mill.cpp',
        'src/lincity/modules/port.cpp',
        'src/lincity/modules/market.cpp',
        'src/lincity/modules/school.cpp',
        'src/lincity/modules/shanty.cpp',
        'src/lincity/modules/commune.cpp',
        'src/lincity/modules/cricket.cpp',
        'src/lincity/modules/oremine.cpp',
        'src/lincity/modules/pottery.cpp',
        'src/lincity/modules/recycle.cpp',
        'src/lincity/modules/coalmine.cpp',
        'src/lincity/modules/monument.cpp',
        'src/lincity/modules/parkland.cpp',
        'src/lincity/modules/water.cpp',
        'src/lincity/modules/windmill.cpp',
        'src/lincity/modules/residence.cpp',
        'src/lincity/modules/waterwell.cpp',
        'src/lincity/modules/windpower.cpp',
        'src/lincity/modules/blacksmith.cpp',
        'src/lincity/modules/coal_power.cpp',
        'src/lincity/modules/power_line.cpp',
        'src/lincity/modules/rocket_pad.cpp',
        'src/lincity/modules/substation.cpp',
        'src/lincity/modules/university.cpp',
        'src/lincity/modules/firestation.cpp',
        'src/lincity/modules/solar_power.cpp',
        'src/lincity/modules/organic_farm.cpp',
        'src/lincity/modules/health_centre.cpp',
        'src/lincity/modules/all_modules.cpp',
        'src/lincity/modules/heavy_industry.cpp',
        'src/lincity/modules/light_industry.cpp',
        'src/lincity/modules/track_road_rail.cpp',

        'src/lincity-ng/PbarInterface.cpp',
        'src/lincity-ng/TimerInterface.cpp',
        'src/lincity-ng/ButtonInterface.cpp',
        'src/lincity-ng/main.cpp',
        'src/lincity-ng/MapEdit.cpp',
        'src/lincity-ng/MainMenu.cpp',
        'src/lincity-ng/ScreenInterface.cpp',
        'src/lincity-ng/Dialog.cpp',
        'src/lincity-ng/Game.cpp',
        'src/lincity-ng/Config.cpp',
        'src/lincity-ng/MainLincity.cpp',
        'src/lincity-ng/Debug.cpp',
        'src/lincity-ng/readdir.cpp',
        'src/lincity-ng/getBundleSharePath.cpp',
        'src/lincity-ng/MiniMap.cpp',
        'src/lincity-ng/ButtonPanel.cpp',
        'src/lincity-ng/GameView.cpp',
        'src/lincity-ng/HelpWindow.cpp',
        'src/lincity-ng/MpsInterface.cpp',
        'src/lincity-ng/Util.cpp',
        'src/lincity-ng/Permutator.cpp',
        'src/lincity-ng/CheckButton.cpp',
        'src/lincity-ng/ReadPngInterface.cpp',
        'src/lincity-ng/Sound.cpp',
        'src/lincity-ng/Mps.cpp',
        'src/lincity-ng/ErrorInterface.cpp',
        'src/lincity-ng/PBar.cpp',
        'src/lincity-ng/EconomyGraph.cpp',
    ],
    include_directories: [
        include_directories('src'),
        include_directories('src/gui'),
        include_directories('src/lincity'),
    ],
    dependencies: [
        physfs,
        sdl,
        dependency('gl'),
        dependency('libxml-2.0'),
        dependency('SDL_gfx'),
        dependency('SDL_image'),
        dependency('SDL_mixer'),
        dependency('SDL_ttf'),
        dependency('threads'),
        dependency('zlib'),
    ],
    link_with: [
        physfsstream,
        tinygettext,
    ],
    link_args: extra_args,
)
