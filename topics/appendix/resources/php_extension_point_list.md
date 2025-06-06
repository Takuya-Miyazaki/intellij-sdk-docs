<!-- Copyright 2000-2025 JetBrains s.r.o. and contributors. Use of this source code is governed by the Apache 2.0 license. -->

<!-- EP List Directory: /phpstorm/ -->

# PHP Extension Point and Listener List

<link-summary>Overview of Extension Points and Listeners for PHP.</link-summary>

<tldr>

**Product-Specific Plugin Development**: [PhpStorm](phpstorm.md)

</tldr>

63 Extension Points and 11 Listeners

See [](intellij_platform_extension_point_list.md) for IntelliJ Platform.

<include from="snippets.topic" element-id="ep_list_legend"/>

## PhpStorm

### PhpStorm – Listeners

| Topic | Listener |
|-------|----------|
| [ComposerInstalledPackagesService#PACKAGE_MANAGER_TOPIC](https://jb.gg/ipe/listeners?topics=com.jetbrains.php.composer.actions.update.ComposerInstalledPackagesService.ComposerUpdateListener)  ![Project-Level][project-level] | `ComposerUpdateListener` |
| [RepositoriesComposerConfig#TOPIC](https://jb.gg/ipe/listeners?topics=com.jetbrains.php.composer.json.cache.ComposerRepositoriesChangedListener)  | `ComposerRepositoriesChangedListener` |
| [StateChangedListener#TOPIC](https://jb.gg/ipe/listeners?topics=com.jetbrains.php.config.PhpProjectSharedConfiguration.StateChangedListener)  | `StateChangedListener` |
| [StateChangedListener#LANGUAGE_LEVEL_CHANGED_TOPIC](https://jb.gg/ipe/listeners?topics=com.jetbrains.php.config.PhpProjectSharedConfiguration.StateChangedListener)  | `StateChangedListener` |
| [PhpProjectWorkspaceConfiguration#TOPIC](https://jb.gg/ipe/listeners?topics=com.jetbrains.php.config.PhpProjectWorkspaceConfigurationListener)  | `PhpProjectWorkspaceConfigurationListener` |
| [DefaultStubsPathListener#TOPIC](https://jb.gg/ipe/listeners?topics=com.jetbrains.php.config.PhpRuntimeConfiguration.DefaultStubsPathListener)  | `DefaultStubsPathListener` |
| [PhpInterpreterConflictResolveListener#TOPIC](https://jb.gg/ipe/listeners?topics=com.jetbrains.php.config.interpreters.PhpInterpretersManagerImpl.PhpInterpreterConflictResolveListener)  | `PhpInterpreterConflictResolveListener` |
| [StateChangedListener#TOPIC](https://jb.gg/ipe/listeners?topics=com.jetbrains.php.debug.listener.PhpDebugExternalConnectionsAccepter.StateChangedListener)  | `StateChangedListener` |
| [RectorChangesListener#TOPIC](https://jb.gg/ipe/listeners?topics=com.jetbrains.php.rector.RectorChangesListener)  | `RectorChangesListener` |
| [PhpRemoteInterpreterChangedListener#TOPIC](https://jb.gg/ipe/listeners?topics=com.jetbrains.php.remote.interpreter.ui.PhpRemoteInterpreterConfigurationForm.PhpRemoteInterpreterChangedListener)  | `PhpRemoteInterpreterChangedListener` |
| [CustomExpectationNotifier.Companion#TOPIC](https://jb.gg/ipe/listeners?topics=com.pestphp.pest.features.customExpectations.CustomExpectationNotifier)  ![Project-Level][project-level] | `CustomExpectationNotifier` |


### com.intellij.phing

| Extension Point | Implementation |
|-----------------|----------------|
| [com.intellij.phing.phpFileDescriptionProvider](https://jb.gg/ipe?extensions=com.intellij.phing.phpFileDescriptionProvider) ![Non-Dynamic][non-dynamic] | `PhingPhpFileDescriptionProvider` |
| [com.intellij.phing.propertyFilesManager](https://jb.gg/ipe?extensions=com.intellij.phing.propertyFilesManager) ![Non-Dynamic][non-dynamic] | `PropertyFilesManager` |

### com.intellij.php.psalm

| Extension Point | Implementation |
|-----------------|----------------|
| [com.jetbrains.php.tools.quality.Psalm.PsalmConfigurationProvider](https://jb.gg/ipe?extensions=com.jetbrains.php.tools.quality.Psalm.PsalmConfigurationProvider) ![Non-Dynamic][non-dynamic] | `PsalmConfigurationProvider` |

### com.intellij.php.tools.quality.phpstan

| Extension Point | Implementation |
|-----------------|----------------|
| [com.jetbrains.php.tools.quality.PhpStan.PhpStanConfigurationProvider](https://jb.gg/ipe?extensions=com.jetbrains.php.tools.quality.PhpStan.PhpStanConfigurationProvider) ![Non-Dynamic][non-dynamic] | `PhpStanConfigurationProvider` |

### com.jetbrains.php

| Extension Point | Implementation |
|-----------------|----------------|
| [com.intellij.php.debug.template.configurable](https://jb.gg/ipe?extensions=com.intellij.php.debug.template.configurable) ![Internal][internal] ![Project-Level][project-level] | `PhpTemplateDebugConfigurable` |
| [com.intellij.php.debug.templateLanguage](https://jb.gg/ipe?extensions=com.intellij.php.debug.templateLanguage) ![Internal][internal] | `PhpTemplateLanguagePathMapper` |
| [com.intellij.php.typeProvider2](https://jb.gg/ipe?extensions=com.intellij.php.typeProvider2) ![Deprecated][deprecated] | `PhpTypeProvider2` |
| [com.intellij.phpDeadCode](https://jb.gg/ipe?extensions=com.intellij.phpDeadCode) | [`EntryPoint`](%gh-ic%/platform/analysis-api/src/com/intellij/codeInspection/reference/EntryPoint.java) |
| [com.intellij.phpRunConfigurationExtension](https://jb.gg/ipe?extensions=com.intellij.phpRunConfigurationExtension) | `PhpRunConfigurationExtension` |
| [com.jetbrains.php.arrayShapesProvider](https://jb.gg/ipe?extensions=com.jetbrains.php.arrayShapesProvider) | `PhpArrayShapesProvider` |
| [com.jetbrains.php.baseLexerProvider](https://jb.gg/ipe?extensions=com.jetbrains.php.baseLexerProvider) ![Internal][internal] | `PhpBaseLexerProvider` |
| [com.jetbrains.php.classAliasProvider](https://jb.gg/ipe?extensions=com.jetbrains.php.classAliasProvider) | `PhpClassAliasProvider` |
| [com.jetbrains.php.composer.execProvider](https://jb.gg/ipe?extensions=com.jetbrains.php.composer.execProvider) | `ComposerExecutionProvider` |
| [com.jetbrains.php.composerConfigClient](https://jb.gg/ipe?extensions=com.jetbrains.php.composerConfigClient) ![Internal][internal] | `ComposerConfigClient` |
| [com.jetbrains.php.config.customFormatFunctionsProvider](https://jb.gg/ipe?extensions=com.jetbrains.php.config.customFormatFunctionsProvider) | `PhpCustomFormatFunctionsProvider` |
| [com.jetbrains.php.config.interpreterFormProvider](https://jb.gg/ipe?extensions=com.jetbrains.php.config.interpreterFormProvider) | `PhpInterpreterFormProvider` |
| [com.jetbrains.php.config.interpreters.PhpInterpretersStateListener](https://jb.gg/ipe?extensions=com.jetbrains.php.config.interpreters.PhpInterpretersStateListener) | `PhpInterpretersStateListener` |
| [com.jetbrains.php.coreMethodProvider](https://jb.gg/ipe?extensions=com.jetbrains.php.coreMethodProvider) ![Internal][internal] | `PhpCoreHandler` |
| [com.jetbrains.php.customFunctionIndex](https://jb.gg/ipe?extensions=com.jetbrains.php.customFunctionIndex) | `PhpCustomFunctionIndex` |
| [com.jetbrains.php.customFunctionPredicate](https://jb.gg/ipe?extensions=com.jetbrains.php.customFunctionPredicate) ![Internal][internal] | `PhpCustomFunctionPredicateIndex` |
| [com.jetbrains.php.customTemplatesNamesProvider](https://jb.gg/ipe?extensions=com.jetbrains.php.customTemplatesNamesProvider) ![Experimental][experimental] | `PhpCustomTemplatesNamesProvider` |
| [com.jetbrains.php.debug.mapping.localPathFixer](https://jb.gg/ipe?extensions=com.jetbrains.php.debug.mapping.localPathFixer) | `PhpLocalPathFixer` |
| [com.jetbrains.php.deprecationFixesProvider](https://jb.gg/ipe?extensions=com.jetbrains.php.deprecationFixesProvider) | `PhpDeprecationQuickFixesProvider` |
| [com.jetbrains.php.deprecationProvider](https://jb.gg/ipe?extensions=com.jetbrains.php.deprecationProvider) | `PhpDeprecationProvider` |
| [com.jetbrains.php.dfaStateFromAssertionProvider](https://jb.gg/ipe?extensions=com.jetbrains.php.dfaStateFromAssertionProvider) ![Internal][internal] | `PhpDfaStateFromAssertionProvider` |
| [com.jetbrains.php.docPrefixProvider](https://jb.gg/ipe?extensions=com.jetbrains.php.docPrefixProvider) ![Internal][internal] | `PhpDocPrefixProvider` |
| [com.jetbrains.php.docTagValuesStubProvider](https://jb.gg/ipe?extensions=com.jetbrains.php.docTagValuesStubProvider) | `PhpCustomDocTagValuesStubProvider` |
| [com.jetbrains.php.expressionClassNamesProvider](https://jb.gg/ipe?extensions=com.jetbrains.php.expressionClassNamesProvider) ![Internal][internal] | `PhpExpressionClassNamesProvider` |
| [com.jetbrains.php.externalUsagesSearcher](https://jb.gg/ipe?extensions=com.jetbrains.php.externalUsagesSearcher) | `PhpExternalUsagesSearcher` |
| [com.jetbrains.php.frameworkProjectConfigurableProvider](https://jb.gg/ipe?extensions=com.jetbrains.php.frameworkProjectConfigurableProvider) | `PhpFrameworkConfigurableProvider` |
| [com.jetbrains.php.frameworkUsageProvider](https://jb.gg/ipe?extensions=com.jetbrains.php.frameworkUsageProvider) | `PhpFrameworkUsageProvider` |
| [com.jetbrains.php.includedPathsContributor](https://jb.gg/ipe?extensions=com.jetbrains.php.includedPathsContributor) | `PhpIncludedPathsContributor` |
| [com.jetbrains.php.injectionExternalFragmentSubstProvider](https://jb.gg/ipe?extensions=com.jetbrains.php.injectionExternalFragmentSubstProvider) ![Project-Level][project-level] | `PhpInjectionExternalFragmentSubstProvider` |
| [com.jetbrains.php.keyTypeProvider](https://jb.gg/ipe?extensions=com.jetbrains.php.keyTypeProvider) ![Internal][internal] | `PhpKeyTypeProvider` |
| [com.jetbrains.php.libraryRoot](https://jb.gg/ipe?extensions=com.jetbrains.php.libraryRoot) ![Internal][internal] | `PhpLibraryRootProvider` |
| [com.jetbrains.php.magicMethodProvider](https://jb.gg/ipe?extensions=com.jetbrains.php.magicMethodProvider) ![Internal][internal] | `PhpMagicHandler` |
| [com.jetbrains.php.metaSignatureResolver](https://jb.gg/ipe?extensions=com.jetbrains.php.metaSignatureResolver) ![Internal][internal] | `PhpMetaSignatureResolver` |
| [com.jetbrains.php.metaTableProvider](https://jb.gg/ipe?extensions=com.jetbrains.php.metaTableProvider) ![Internal][internal] | `PhpMetaTableProvider` |
| [com.jetbrains.php.noReturnProvider](https://jb.gg/ipe?extensions=com.jetbrains.php.noReturnProvider) | `PhpNoReturnProvider` |
| [com.jetbrains.php.openSettingsProvider](https://jb.gg/ipe?extensions=com.jetbrains.php.openSettingsProvider) | `Settings` |
| [com.jetbrains.php.phpunit.phpUnitSettingsLoader](https://jb.gg/ipe?extensions=com.jetbrains.php.phpunit.phpUnitSettingsLoader) ![Internal][internal] | `PhpUnitSettingsLoader` |
| [com.jetbrains.php.predefinedVariableProvider](https://jb.gg/ipe?extensions=com.jetbrains.php.predefinedVariableProvider) | `PhpPredefinedVariableProvider` |
| [com.jetbrains.php.referenceResolver2](https://jb.gg/ipe?extensions=com.jetbrains.php.referenceResolver2) | `PhpMultipleDeclarationFilter` |
| [com.jetbrains.php.referenceScopeExtension](https://jb.gg/ipe?extensions=com.jetbrains.php.referenceScopeExtension) ![Experimental][experimental] | `PhpReferenceScopeExtension` |
| [com.jetbrains.php.relatedToPhpFilesContributor](https://jb.gg/ipe?extensions=com.jetbrains.php.relatedToPhpFilesContributor) | `RelatedToPhpFilesContributor` |
| [com.jetbrains.php.remote.remoteInterpreterManager](https://jb.gg/ipe?extensions=com.jetbrains.php.remote.remoteInterpreterManager) | `PhpRemoteInterpreterManager` |
| [com.jetbrains.php.templateLanguageHighlightingExtension](https://jb.gg/ipe?extensions=com.jetbrains.php.templateLanguageHighlightingExtension) ![Internal][internal] | `TemplateLanguageBackgroundColorProvider` |
| [com.jetbrains.php.testFramework.phpTestOldConfigHolder](https://jb.gg/ipe?extensions=com.jetbrains.php.testFramework.phpTestOldConfigHolder) ![Deprecated][deprecated] ![Internal][internal] | `PhpTestFrameworkOldConfigHolder` |
| [com.jetbrains.php.testFrameworkType](https://jb.gg/ipe?extensions=com.jetbrains.php.testFrameworkType) | `PhpTestFrameworkType` |
| [com.jetbrains.php.tools.quality.laravelPint.laravelPintConfigurationProvider](https://jb.gg/ipe?extensions=com.jetbrains.php.tools.quality.laravelPint.laravelPintConfigurationProvider) | `LaravelPintConfigurationProvider` |
| [com.jetbrains.php.tools.quality.messDetector.messDetectorConfigurationProvider](https://jb.gg/ipe?extensions=com.jetbrains.php.tools.quality.messDetector.messDetectorConfigurationProvider) | `MessDetectorConfigurationProvider` |
| [com.jetbrains.php.tools.quality.phpCSFixer.phpCSFixerConfigurationProvider](https://jb.gg/ipe?extensions=com.jetbrains.php.tools.quality.phpCSFixer.phpCSFixerConfigurationProvider) | `PhpCSFixerConfigurationProvider` |
| [com.jetbrains.php.tools.quality.phpcs.phpCSConfigurationProvider](https://jb.gg/ipe?extensions=com.jetbrains.php.tools.quality.phpcs.phpCSConfigurationProvider) | `PhpCSConfigurationProvider` |
| [com.jetbrains.php.tools.quality.type](https://jb.gg/ipe?extensions=com.jetbrains.php.tools.quality.type) | `QualityToolType` |
| [com.jetbrains.php.typeProvider3](https://jb.gg/ipe?extensions=com.jetbrains.php.typeProvider3) ![Deprecated][deprecated] | `PhpTypeProvider3` |
| [com.jetbrains.php.typeProvider4](https://jb.gg/ipe?extensions=com.jetbrains.php.typeProvider4) | `PhpTypeProvider4` |

### com.jetbrains.php.behat

| Extension Point | Implementation |
|-----------------|----------------|
| [com.jetbrains.php.behat.gherkinContextProvider](https://jb.gg/ipe?extensions=com.jetbrains.php.behat.gherkinContextProvider) | `ContextInterfaceProvider` |

### com.jetbrains.php.blade

| Extension Point | Implementation |
|-----------------|----------------|
| [com.jetbrains.php.blade.bladeDirectiveContributor](https://jb.gg/ipe?extensions=com.jetbrains.php.blade.bladeDirectiveContributor) ![Experimental][experimental] | `BladeDirectiveContributor` |

### com.jetbrains.php.framework

| Extension Point | Implementation |
|-----------------|----------------|
| [com.jetbrains.php.framework.descriptionProvider](https://jb.gg/ipe?extensions=com.jetbrains.php.framework.descriptionProvider) ![Internal][internal] | `FrameworkDescriptionProvider` |

### intellij.php.frontback.impl.xml

| Extension Point | Implementation |
|-----------------|----------------|
| [com.intellij.php.docTagParserExtension](https://jb.gg/ipe?extensions=com.intellij.php.docTagParserExtension) ![Internal][internal] | `PhpDocTagParser` |

### phpstorm-remote-interpreter-plugin.xml

| Extension Point | Implementation |
|-----------------|----------------|
| [com.jetbrains.php.remote.interpreter.ui.customConfigProvider](https://jb.gg/ipe?extensions=com.jetbrains.php.remote.interpreter.ui.customConfigProvider) | `PhpProjectConfigComponentProvider` |
| [com.jetbrains.php.remote.phpHelperScriptProvider](https://jb.gg/ipe?extensions=com.jetbrains.php.remote.phpHelperScriptProvider) | `PhpHelperScriptProvider` |
| [com.jetbrains.php.remote.remoteProcessManager](https://jb.gg/ipe?extensions=com.jetbrains.php.remote.remoteProcessManager) | `PhpRemoteProcessManager` |

[deprecated]: https://img.shields.io/badge/-Deprecated-lightgrey?style=flat-square
[removal]: https://img.shields.io/badge/-Removal-red?style=flat-square
[obsolete]: https://img.shields.io/badge/-Obsolete-grey?style=flat-square
[experimental]: https://img.shields.io/badge/-Experimental-violet?style=flat-square
[internal]: https://img.shields.io/badge/-Internal-darkred?style=flat-square
[project-level]: https://img.shields.io/badge/-Project--Level-blue?style=flat-square
[non-dynamic]: https://img.shields.io/badge/-Non--Dynamic-orange?style=flat-square
[dumb-aware]: https://img.shields.io/badge/-DumbAware-darkgreen?style=flat-square
