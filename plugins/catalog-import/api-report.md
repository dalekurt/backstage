## API Report File for "@backstage/plugin-catalog-import"

> Do not edit this file. It is a report generated by [API Extractor](https://api-extractor.com/).

```ts
/// <reference types="react" />

import { ApiRef } from '@backstage/core-plugin-api';
import { BackstagePlugin } from '@backstage/core-plugin-api';
import { CatalogApi } from '@backstage/catalog-client';
import { ConfigApi } from '@backstage/core-plugin-api';
import { Controller } from 'react-hook-form';
import { DiscoveryApi } from '@backstage/core-plugin-api';
import { Entity } from '@backstage/catalog-model';
import { EntityName } from '@backstage/catalog-model';
import { FieldErrors } from 'react-hook-form';
import { IdentityApi } from '@backstage/core-plugin-api';
import { InfoCardVariants } from '@backstage/core-components';
import { OAuthApi } from '@backstage/core-plugin-api';
import { default as React_2 } from 'react';
import { RouteRef } from '@backstage/core-plugin-api';
import { ScmIntegrationRegistry } from '@backstage/integration';
import { SubmitHandler } from 'react-hook-form';
import { TextFieldProps } from '@material-ui/core/TextField/TextField';
import { UnpackNestedValue } from 'react-hook-form';
import { UseFormProps } from 'react-hook-form';
import { UseFormReturn } from 'react-hook-form';

// Warning: (ae-missing-release-tag) "AnalyzeResult" is exported by the package, but it is missing a release tag (@alpha, @beta, @public, or @internal)
//
// @public (undocumented)
export type AnalyzeResult =
  | {
      type: 'locations';
      locations: Array<{
        target: string;
        entities: EntityName[];
      }>;
    }
  | {
      type: 'repository';
      url: string;
      integrationType: string;
      generatedEntities: PartialEntity[];
    };

// Warning: (ae-forgotten-export) The symbol "Props" needs to be exported by the entry point index.d.ts
// Warning: (ae-missing-release-tag) "AutocompleteTextField" is exported by the package, but it is missing a release tag (@alpha, @beta, @public, or @internal)
//
// @public (undocumented)
export const AutocompleteTextField: <TFieldValue extends string>({
  name,
  options,
  required,
  errors,
  rules,
  loading,
  loadingText,
  helperText,
  errorHelperText,
  textFieldProps,
}: Props_4<TFieldValue>) => JSX.Element;

// Warning: (ae-missing-release-tag) "CatalogImportApi" is exported by the package, but it is missing a release tag (@alpha, @beta, @public, or @internal)
//
// @public (undocumented)
export interface CatalogImportApi {
  // (undocumented)
  analyzeUrl(url: string): Promise<AnalyzeResult>;
  // (undocumented)
  submitPullRequest(options: {
    repositoryUrl: string;
    fileContent: string;
    title: string;
    body: string;
  }): Promise<{
    link: string;
    location: string;
  }>;
}

// Warning: (ae-missing-release-tag) "catalogImportApiRef" is exported by the package, but it is missing a release tag (@alpha, @beta, @public, or @internal)
//
// @public (undocumented)
export const catalogImportApiRef: ApiRef<CatalogImportApi>;

// Warning: (ae-missing-release-tag) "CatalogImportClient" is exported by the package, but it is missing a release tag (@alpha, @beta, @public, or @internal)
//
// @public (undocumented)
export class CatalogImportClient implements CatalogImportApi {
  constructor(options: {
    discoveryApi: DiscoveryApi;
    githubAuthApi: OAuthApi;
    identityApi: IdentityApi;
    scmIntegrationsApi: ScmIntegrationRegistry;
    catalogApi: CatalogApi;
  });
  // (undocumented)
  analyzeUrl(url: string): Promise<AnalyzeResult>;
  // (undocumented)
  submitPullRequest({
    repositoryUrl,
    fileContent,
    title,
    body,
  }: {
    repositoryUrl: string;
    fileContent: string;
    title: string;
    body: string;
  }): Promise<{
    link: string;
    location: string;
  }>;
}

// Warning: (ae-forgotten-export) The symbol "StepperProviderOpts" needs to be exported by the entry point index.d.ts
// Warning: (ae-missing-release-tag) "CatalogImportPage" is exported by the package, but it is missing a release tag (@alpha, @beta, @public, or @internal)
//
// @public (undocumented)
export const CatalogImportPage: (opts: StepperProviderOpts) => JSX.Element;

// Warning: (ae-missing-release-tag) "catalogImportPlugin" is exported by the package, but it is missing a release tag (@alpha, @beta, @public, or @internal)
//
// @public (undocumented)
const catalogImportPlugin: BackstagePlugin<
  {
    importPage: RouteRef<undefined>;
  },
  {}
>;
export { catalogImportPlugin };
export { catalogImportPlugin as plugin };

// Warning: (tsdoc-param-tag-missing-hyphen) The @param block should be followed by a parameter name and then a hyphen
// Warning: (tsdoc-param-tag-missing-hyphen) The @param block should be followed by a parameter name and then a hyphen
// Warning: (ae-forgotten-export) The symbol "ImportFlows" needs to be exported by the entry point index.d.ts
// Warning: (ae-forgotten-export) The symbol "StepperProvider" needs to be exported by the entry point index.d.ts
// Warning: (ae-missing-release-tag) "defaultGenerateStepper" is exported by the package, but it is missing a release tag (@alpha, @beta, @public, or @internal)
//
// @public
export function defaultGenerateStepper(
  flow: ImportFlows,
  defaults: StepperProvider,
): StepperProvider;

// Warning: (ae-forgotten-export) The symbol "Props" needs to be exported by the entry point index.d.ts
// Warning: (ae-missing-release-tag) "EntityListComponent" is exported by the package, but it is missing a release tag (@alpha, @beta, @public, or @internal)
//
// @public (undocumented)
export const EntityListComponent: ({
  locations,
  collapsed,
  locationListItemIcon,
  onItemClick,
  firstListItem,
  withLinks,
}: Props_2) => JSX.Element;

// Warning: (ae-forgotten-export) The symbol "Props" needs to be exported by the entry point index.d.ts
// Warning: (ae-missing-release-tag) "ImportStepper" is exported by the package, but it is missing a release tag (@alpha, @beta, @public, or @internal)
//
// @public (undocumented)
export const ImportStepper: ({
  initialUrl,
  generateStepper,
  variant,
  opts,
}: Props) => JSX.Element;

// Warning: (tsdoc-param-tag-missing-hyphen) The @param block should be followed by a parameter name and then a hyphen
// Warning: (tsdoc-param-tag-missing-hyphen) The @param block should be followed by a parameter name and then a hyphen
// Warning: (tsdoc-param-tag-missing-hyphen) The @param block should be followed by a parameter name and then a hyphen
// Warning: (ae-forgotten-export) The symbol "Props" needs to be exported by the entry point index.d.ts
// Warning: (ae-missing-release-tag) "PreparePullRequestForm" is exported by the package, but it is missing a release tag (@alpha, @beta, @public, or @internal)
//
// @public
export const PreparePullRequestForm: <
  TFieldValues extends Record<string, any>,
>({
  defaultValues,
  onSubmit,
  render,
}: Props_5<TFieldValues>) => JSX.Element;

// Warning: (ae-forgotten-export) The symbol "Props" needs to be exported by the entry point index.d.ts
// Warning: (ae-missing-release-tag) "PreviewCatalogInfoComponent" is exported by the package, but it is missing a release tag (@alpha, @beta, @public, or @internal)
//
// @public (undocumented)
export const PreviewCatalogInfoComponent: ({
  repositoryUrl,
  entities,
  classes,
}: Props_6) => JSX.Element;

// Warning: (ae-forgotten-export) The symbol "Props" needs to be exported by the entry point index.d.ts
// Warning: (ae-missing-release-tag) "PreviewPullRequestComponent" is exported by the package, but it is missing a release tag (@alpha, @beta, @public, or @internal)
//
// @public (undocumented)
export const PreviewPullRequestComponent: ({
  title,
  description,
  classes,
}: Props_7) => JSX.Element;

// Warning: (ae-missing-release-tag) "Router" is exported by the package, but it is missing a release tag (@alpha, @beta, @public, or @internal)
//
// @public (undocumented)
export const Router: (opts: StepperProviderOpts) => JSX.Element;

// Warning: (tsdoc-param-tag-missing-hyphen) The @param block should be followed by a parameter name and then a hyphen
// Warning: (tsdoc-param-tag-missing-hyphen) The @param block should be followed by a parameter name and then a hyphen
// Warning: (tsdoc-param-tag-missing-hyphen) The @param block should be followed by a parameter name and then a hyphen
// Warning: (ae-forgotten-export) The symbol "Props" needs to be exported by the entry point index.d.ts
// Warning: (ae-missing-release-tag) "StepInitAnalyzeUrl" is exported by the package, but it is missing a release tag (@alpha, @beta, @public, or @internal)
//
// @public
export const StepInitAnalyzeUrl: ({
  onAnalysis,
  analysisUrl,
  disablePullRequest,
}: Props_3) => JSX.Element;

// Warning: (ae-forgotten-export) The symbol "Props" needs to be exported by the entry point index.d.ts
// Warning: (ae-missing-release-tag) "StepPrepareCreatePullRequest" is exported by the package, but it is missing a release tag (@alpha, @beta, @public, or @internal)
//
// @public (undocumented)
export const StepPrepareCreatePullRequest: ({
  analyzeResult,
  onPrepare,
  onGoBack,
  renderFormFields,
  defaultTitle,
  defaultBody,
}: Props_8) => JSX.Element;

// Warnings were encountered during analysis:
//
// src/api/CatalogImportApi.d.ts:14:5 - (ae-forgotten-export) The symbol "PartialEntity" needs to be exported by the entry point index.d.ts

// (No @packageDocumentation comment for this package)
```