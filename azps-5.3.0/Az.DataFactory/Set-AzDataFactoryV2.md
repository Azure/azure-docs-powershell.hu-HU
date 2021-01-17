---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2.md
ms.openlocfilehash: 5020ddeccc755ef52bf7410d61eb57b637d261bf
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480391"
---
# <span data-ttu-id="e9206-101">Set-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="e9206-101">Set-AzDataFactoryV2</span></span>

## <span data-ttu-id="e9206-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9206-102">SYNOPSIS</span></span>
<span data-ttu-id="e9206-103">Adatüzemet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="e9206-103">Creates a data factory.</span></span>

## <span data-ttu-id="e9206-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e9206-104">SYNTAX</span></span>

### <span data-ttu-id="e9206-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e9206-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>]
 [-Force]
 [-GlobalParameterDefinition <System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9206-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e9206-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2 [-ResourceId] <String> [-Location] <String> [[-Tag] <Hashtable>] [-Force]
 [-GlobalParameterDefinition <System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9206-107">ByResourceIdFactoryRepoVstsConfig</span><span class="sxs-lookup"><span data-stu-id="e9206-107">ByResourceIdFactoryRepoVstsConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceId] <String> [-Location] <String> [[-Tag] <Hashtable>] [-Force]
 [-GlobalParameterDefinition <System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]>]
 -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -ProjectName <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9206-108">ByResourceIdFactoryRepoGitConfig</span><span class="sxs-lookup"><span data-stu-id="e9206-108">ByResourceIdFactoryRepoGitConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceId] <String> [-Location] <String> [[-Tag] <Hashtable>] [-Force]
 [-GlobalParameterDefinition <System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]>]
 -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -HostName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e9206-109">ByFactoryNameFactoryRepoGitConfig</span><span class="sxs-lookup"><span data-stu-id="e9206-109">ByFactoryNameFactoryRepoGitConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>]
 [-Force]
 [-GlobalParameterDefinition <System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]>]
 -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -HostName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e9206-110">ByFactoryNameFactoryRepoVstsConfig</span><span class="sxs-lookup"><span data-stu-id="e9206-110">ByFactoryNameFactoryRepoVstsConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>]
 [-Force]
 [-GlobalParameterDefinition <System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]>]
 -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -ProjectName <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9206-111">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="e9206-111">ByInputObject</span></span>
```
Set-AzDataFactoryV2 -InputObject <PSDataFactory> [[-Location] <String>] [[-Tag] <Hashtable>] [-Force]
 [-GlobalParameterDefinition <System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9206-112">ByInputObjectFactoryRepoVstsConfig</span><span class="sxs-lookup"><span data-stu-id="e9206-112">ByInputObjectFactoryRepoVstsConfig</span></span>
```
Set-AzDataFactoryV2 -InputObject <PSDataFactory> [[-Location] <String>] [[-Tag] <Hashtable>] [-Force]
 [-GlobalParameterDefinition <System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]>]
 [-AccountName <String>] [-RepositoryName <String>] [-CollaborationBranch <String>] [-RootFolder <String>]
 [-LastCommitId <String>] -ProjectName <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9206-113">ByInputObjectFactoryRepoGitConfig</span><span class="sxs-lookup"><span data-stu-id="e9206-113">ByInputObjectFactoryRepoGitConfig</span></span>
```
Set-AzDataFactoryV2 -InputObject <PSDataFactory> [[-Location] <String>] [[-Tag] <Hashtable>] [-Force]
 [-GlobalParameterDefinition <System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]>]
 [-AccountName <String>] [-RepositoryName <String>] [-CollaborationBranch <String>] [-RootFolder <String>]
 [-LastCommitId <String>] -HostName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e9206-114">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e9206-114">DESCRIPTION</span></span>
<span data-ttu-id="e9206-115">A **Set-AzDataFactoryV2** parancsmag létrehoz egy adatüzemet a megadott erőforráscsoport nevével és helyével.</span><span class="sxs-lookup"><span data-stu-id="e9206-115">The **Set-AzDataFactoryV2** cmdlet creates a data factory with the specified resource group name and location.</span></span>
<span data-ttu-id="e9206-116">Végezze el ezeket a műveleteket a következő sorrendben: - Adatüzem létrehozása.</span><span class="sxs-lookup"><span data-stu-id="e9206-116">Perform these operations in the following order: -- Create a data factory.</span></span>
<span data-ttu-id="e9206-117">– Csatolt szolgáltatások létrehozása.</span><span class="sxs-lookup"><span data-stu-id="e9206-117">-- Create linked services.</span></span>
<span data-ttu-id="e9206-118">– Adatkészletek létrehozása.</span><span class="sxs-lookup"><span data-stu-id="e9206-118">-- Create datasets.</span></span>
<span data-ttu-id="e9206-119">– Folyamat létrehozása.</span><span class="sxs-lookup"><span data-stu-id="e9206-119">-- Create a pipeline.</span></span>

## <span data-ttu-id="e9206-120">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e9206-120">EXAMPLES</span></span>

### <span data-ttu-id="e9206-121">1. példa: Adat factory létrehozása</span><span class="sxs-lookup"><span data-stu-id="e9206-121">Example 1: Create a data factory</span></span>
```
PS C:\> Set-AzDataFactoryV2 -ResourceGroupName "ADF" -Name "WikiADF" -Location "WestUS"

    DataFactoryName   : WikiADF
    DataFactoryId     : /subscriptions/3e8e61b5-9a7d-4952-bfae-545ab997b9ea/resourceGroups/adf/providers/Microsoft.DataFactory/factories/wikiadf
    ResourceGroupName : ADF
    Location          : EastUS
    Tags              : {}
    Identity          : Microsoft.Azure.Management.DataFactory.Models.FactoryIdentity
    ProvisioningState : Succeeded
    RepoConfiguration :
```

### <span data-ttu-id="e9206-122">2. példa: Adatüzem létrehozása a repo konfigurációs adataival egy meglévő gyári objektum használatával.</span><span class="sxs-lookup"><span data-stu-id="e9206-122">Example 2: Create a data factory with repo configuration details using an existing factory object.</span></span>
```
PS C:\> Get-AzDataFactoryV2 -ResourceGroupName "ADF" -Name "WikiADF" | Set-AzDataFactoryV2 -AccountName msdata -RepositoryName ADFRepo -CollaborationBranch master -RootFolder / -ProjectName "Azure Data Factory"

    DataFactoryName   : WikiADF
    DataFactoryId     : /subscriptions/3e8e61b5-9a7d-4952-bfae-545ab997b9ea/resourceGroups/adf/providers/Microsoft.DataFactory/factories/wikiadf
    ResourceGroupName : ADF
    Location          : EastUS
    Tags              : {}
    Identity          : Microsoft.Azure.Management.DataFactory.Models.FactoryIdentity
    ProvisioningState : Succeeded
    RepoConfiguration : Microsoft.Azure.Management.DataFactory.Models.FactoryVSTSConfiguration
```

<span data-ttu-id="e9206-123">Ez a parancs létrehoz egy WikiADF nevű adatüzemet az ADF nevű erőforráscsoportban az EastUS-helyen az Azure DevOps forrásvezérlő konfigurációval.</span><span class="sxs-lookup"><span data-stu-id="e9206-123">This command creates a data factory named WikiADF in the resource group named ADF in the EastUS location with Azure DevOps source control configuration.</span></span>

### <span data-ttu-id="e9206-124">3. példa: Adatüzem létrehozása a GitHub repo konfigurációs adataival egy új gyári objektum használatával.</span><span class="sxs-lookup"><span data-stu-id="e9206-124">Example 3: Create a data factory with GitHub repo configuration details using a new factory object.</span></span>
```
PS C:\> New-AzDataFactoryV2 -ResourceGroupName "ADF" -Name "WikiADF" -Location 'EastUS' -HostName 'https://github.com' -AccountName msdata -RepositoryName ADFRepo -CollaborationBranch master -RootFolder /

    DataFactoryName   : WikiADF
    DataFactoryId     : /subscriptions/3e8e61b5-9a7d-4952-bfae-545ab997b9ea/resourceGroups/adf/providers/Microsoft.DataFactory/factories/wikiadf
    ResourceGroupName : ADF
    Location          : EastUS
    Tags              : {}
    Identity          : Microsoft.Azure.Management.DataFactory.Models.FactoryIdentity
    ProvisioningState : Succeeded
    RepoConfiguration : Microsoft.Azure.Management.DataFactory.Models.FactoryGitHubConfiguration
```

<span data-ttu-id="e9206-125">Ez a parancs létrehoz egy WikiADF nevű adatüzemet az ADF nevű erőforráscsoportban az EastUS-helyen a GitHub forrásvezérlő-konfigurációval.</span><span class="sxs-lookup"><span data-stu-id="e9206-125">This command creates a data factory named WikiADF in the resource group named ADF in the EastUS location with GitHub source control configuration..</span></span>

## <span data-ttu-id="e9206-126">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e9206-126">PARAMETERS</span></span>

### <span data-ttu-id="e9206-127">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e9206-127">-AccountName</span></span>
<span data-ttu-id="e9206-128">A repo-konfiguráció fiókneve.</span><span class="sxs-lookup"><span data-stu-id="e9206-128">The account name for repo configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdFactoryRepoVstsConfig, ByResourceIdFactoryRepoGitConfig, ByFactoryNameFactoryRepoGitConfig, ByFactoryNameFactoryRepoVstsConfig
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByInputObjectFactoryRepoVstsConfig, ByInputObjectFactoryRepoGitConfig
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9206-129">-CollaborationBranch</span><span class="sxs-lookup"><span data-stu-id="e9206-129">-CollaborationBranch</span></span>
<span data-ttu-id="e9206-130">A repo-konfiguráció együttműködési ága.</span><span class="sxs-lookup"><span data-stu-id="e9206-130">The collaboration branch for repo configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdFactoryRepoVstsConfig, ByResourceIdFactoryRepoGitConfig, ByFactoryNameFactoryRepoGitConfig, ByFactoryNameFactoryRepoVstsConfig
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByInputObjectFactoryRepoVstsConfig, ByInputObjectFactoryRepoGitConfig
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9206-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9206-131">-DefaultProfile</span></span>
<span data-ttu-id="e9206-132">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e9206-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9206-133">-Force</span><span class="sxs-lookup"><span data-stu-id="e9206-133">-Force</span></span>
<span data-ttu-id="e9206-134">A parancsmag futtatása megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="e9206-134">Runs the cmdlet without prompting for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9206-135">-GlobalParameterDefinition</span><span class="sxs-lookup"><span data-stu-id="e9206-135">-GlobalParameterDefinition</span></span>
<span data-ttu-id="e9206-136">Az adatüzem globális paramétereit tartalmazó szótár.</span><span class="sxs-lookup"><span data-stu-id="e9206-136">The dictionary containing the global parameters of the data factory.</span></span>

```yaml
Type: System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9206-137">-HostName</span><span class="sxs-lookup"><span data-stu-id="e9206-137">-HostName</span></span>
<span data-ttu-id="e9206-138">A GitHub repo-konfigurációjának állomásneve.</span><span class="sxs-lookup"><span data-stu-id="e9206-138">The host name for GitHub repo configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdFactoryRepoGitConfig, ByFactoryNameFactoryRepoGitConfig, ByInputObjectFactoryRepoGitConfig
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9206-139">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e9206-139">-InputObject</span></span>
<span data-ttu-id="e9206-140">A data factory objektum.</span><span class="sxs-lookup"><span data-stu-id="e9206-140">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByInputObject, ByInputObjectFactoryRepoVstsConfig, ByInputObjectFactoryRepoGitConfig
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e9206-141">-LastCommitId</span><span class="sxs-lookup"><span data-stu-id="e9206-141">-LastCommitId</span></span>
<span data-ttu-id="e9206-142">A repo-konfiguráció utolsó véglegesítési azonosítója.</span><span class="sxs-lookup"><span data-stu-id="e9206-142">The last commit id for repo configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdFactoryRepoVstsConfig, ByResourceIdFactoryRepoGitConfig, ByFactoryNameFactoryRepoGitConfig, ByFactoryNameFactoryRepoVstsConfig, ByInputObjectFactoryRepoVstsConfig, ByInputObjectFactoryRepoGitConfig
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9206-143">-Location</span><span class="sxs-lookup"><span data-stu-id="e9206-143">-Location</span></span>
<span data-ttu-id="e9206-144">Ebben a régióban jön létre az adatüzem.</span><span class="sxs-lookup"><span data-stu-id="e9206-144">The data factory is created in this region.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByResourceId, ByResourceIdFactoryRepoVstsConfig, ByResourceIdFactoryRepoGitConfig, ByFactoryNameFactoryRepoGitConfig, ByFactoryNameFactoryRepoVstsConfig
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByInputObject, ByInputObjectFactoryRepoVstsConfig, ByInputObjectFactoryRepoGitConfig
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9206-145">-Name</span><span class="sxs-lookup"><span data-stu-id="e9206-145">-Name</span></span>
<span data-ttu-id="e9206-146">Az adatüzem neve.</span><span class="sxs-lookup"><span data-stu-id="e9206-146">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByFactoryNameFactoryRepoGitConfig, ByFactoryNameFactoryRepoVstsConfig
Aliases: DataFactoryName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9206-147">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="e9206-147">-ProjectName</span></span>
<span data-ttu-id="e9206-148">A projekt neve Azure DevOps a repo konfigurációhoz.</span><span class="sxs-lookup"><span data-stu-id="e9206-148">The project name Azure DevOps for repo configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdFactoryRepoVstsConfig, ByFactoryNameFactoryRepoVstsConfig, ByInputObjectFactoryRepoVstsConfig
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9206-149">-RepositoryName</span><span class="sxs-lookup"><span data-stu-id="e9206-149">-RepositoryName</span></span>
<span data-ttu-id="e9206-150">A repo-konfiguráció tárának neve.</span><span class="sxs-lookup"><span data-stu-id="e9206-150">The repository name for repo configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdFactoryRepoVstsConfig, ByResourceIdFactoryRepoGitConfig, ByFactoryNameFactoryRepoGitConfig, ByFactoryNameFactoryRepoVstsConfig
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByInputObjectFactoryRepoVstsConfig, ByInputObjectFactoryRepoGitConfig
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9206-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9206-151">-ResourceGroupName</span></span>
<span data-ttu-id="e9206-152">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e9206-152">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByFactoryNameFactoryRepoGitConfig, ByFactoryNameFactoryRepoVstsConfig
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9206-153">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e9206-153">-ResourceId</span></span>
<span data-ttu-id="e9206-154">A V2 data factory Azure-erőforrásazonosítója.</span><span class="sxs-lookup"><span data-stu-id="e9206-154">The Azure resource ID of V2 data factory.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId, ByResourceIdFactoryRepoVstsConfig, ByResourceIdFactoryRepoGitConfig
Aliases: Id, DataFactoryId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9206-155">-RootFolder</span><span class="sxs-lookup"><span data-stu-id="e9206-155">-RootFolder</span></span>
<span data-ttu-id="e9206-156">A repo-konfiguráció gyökérmappa.</span><span class="sxs-lookup"><span data-stu-id="e9206-156">The root folder for repo configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdFactoryRepoVstsConfig, ByResourceIdFactoryRepoGitConfig, ByFactoryNameFactoryRepoGitConfig, ByFactoryNameFactoryRepoVstsConfig
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByInputObjectFactoryRepoVstsConfig, ByInputObjectFactoryRepoGitConfig
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9206-157">-Tag</span><span class="sxs-lookup"><span data-stu-id="e9206-157">-Tag</span></span>
<span data-ttu-id="e9206-158">Az adatüzem címkéi.</span><span class="sxs-lookup"><span data-stu-id="e9206-158">The tags of the data factory.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByFactoryName, ByResourceId, ByResourceIdFactoryRepoVstsConfig, ByResourceIdFactoryRepoGitConfig, ByFactoryNameFactoryRepoGitConfig, ByFactoryNameFactoryRepoVstsConfig
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByInputObject, ByInputObjectFactoryRepoVstsConfig, ByInputObjectFactoryRepoGitConfig
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9206-159">-TenantId</span><span class="sxs-lookup"><span data-stu-id="e9206-159">-TenantId</span></span>
<span data-ttu-id="e9206-160">Az Azure DevOps repo konfigurációjának bérlőazonosítója.</span><span class="sxs-lookup"><span data-stu-id="e9206-160">The tenant id for Azure DevOps repo configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdFactoryRepoVstsConfig, ByFactoryNameFactoryRepoVstsConfig, ByInputObjectFactoryRepoVstsConfig
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9206-161">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e9206-161">-Confirm</span></span>
<span data-ttu-id="e9206-162">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="e9206-162">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9206-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9206-163">-WhatIf</span></span>
<span data-ttu-id="e9206-164">Azt mutatja, mi történik, ha a parancsmag fut, de nem futtatja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="e9206-164">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9206-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9206-165">CommonParameters</span></span>
<span data-ttu-id="e9206-166">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9206-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9206-167">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e9206-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9206-168">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e9206-168">INPUTS</span></span>

### <span data-ttu-id="e9206-169">System.String</span><span class="sxs-lookup"><span data-stu-id="e9206-169">System.String</span></span>

### <span data-ttu-id="e9206-170">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="e9206-170">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

### <span data-ttu-id="e9206-171">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="e9206-171">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e9206-172">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e9206-172">OUTPUTS</span></span>

### <span data-ttu-id="e9206-173">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="e9206-173">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="e9206-174">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e9206-174">NOTES</span></span>
<span data-ttu-id="e9206-175">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, adatok, faktorok</span><span class="sxs-lookup"><span data-stu-id="e9206-175">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="e9206-176">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e9206-176">RELATED LINKS</span></span>

[<span data-ttu-id="e9206-177">Get-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="e9206-177">Get-AzDataFactoryV2</span></span>]()

[<span data-ttu-id="e9206-178">Remove-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="e9206-178">Remove-AzDataFactoryV2</span></span>]()
