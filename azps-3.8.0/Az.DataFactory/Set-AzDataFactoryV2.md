---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2.md
ms.openlocfilehash: 219e5b18a04332d2ee840fb41b92aa9d282a1792
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847161"
---
# <span data-ttu-id="798d8-101">Set-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="798d8-101">Set-AzDataFactoryV2</span></span>

## <span data-ttu-id="798d8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="798d8-102">SYNOPSIS</span></span>
<span data-ttu-id="798d8-103">Adatfeldolgozót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="798d8-103">Creates a data factory.</span></span>

## <span data-ttu-id="798d8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="798d8-104">SYNTAX</span></span>

### <span data-ttu-id="798d8-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="798d8-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="798d8-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="798d8-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2 [-ResourceId] <String> [-Location] <String> [[-Tag] <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="798d8-107">ByResourceIdFactoryRepoVstsConfig</span><span class="sxs-lookup"><span data-stu-id="798d8-107">ByResourceIdFactoryRepoVstsConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceId] <String> [-Location] <String> [[-Tag] <Hashtable>] [-Force]
 -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -ProjectName <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="798d8-108">ByResourceIdFactoryRepoGitConfig</span><span class="sxs-lookup"><span data-stu-id="798d8-108">ByResourceIdFactoryRepoGitConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceId] <String> [-Location] <String> [[-Tag] <Hashtable>] [-Force]
 -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -HostName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="798d8-109">ByFactoryNameFactoryRepoGitConfig</span><span class="sxs-lookup"><span data-stu-id="798d8-109">ByFactoryNameFactoryRepoGitConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>]
 [-Force] -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -HostName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="798d8-110">ByFactoryNameFactoryRepoVstsConfig</span><span class="sxs-lookup"><span data-stu-id="798d8-110">ByFactoryNameFactoryRepoVstsConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>]
 [-Force] -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -ProjectName <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="798d8-111">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="798d8-111">ByInputObject</span></span>
```
Set-AzDataFactoryV2 -InputObject <PSDataFactory> [[-Location] <String>] [[-Tag] <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="798d8-112">ByInputObjectFactoryRepoVstsConfig</span><span class="sxs-lookup"><span data-stu-id="798d8-112">ByInputObjectFactoryRepoVstsConfig</span></span>
```
Set-AzDataFactoryV2 -InputObject <PSDataFactory> [[-Location] <String>] [[-Tag] <Hashtable>] [-Force]
 [-AccountName <String>] [-RepositoryName <String>] [-CollaborationBranch <String>] [-RootFolder <String>]
 [-LastCommitId <String>] -ProjectName <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="798d8-113">ByInputObjectFactoryRepoGitConfig</span><span class="sxs-lookup"><span data-stu-id="798d8-113">ByInputObjectFactoryRepoGitConfig</span></span>
```
Set-AzDataFactoryV2 -InputObject <PSDataFactory> [[-Location] <String>] [[-Tag] <Hashtable>] [-Force]
 [-AccountName <String>] [-RepositoryName <String>] [-CollaborationBranch <String>] [-RootFolder <String>]
 [-LastCommitId <String>] -HostName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="798d8-114">Leírás</span><span class="sxs-lookup"><span data-stu-id="798d8-114">DESCRIPTION</span></span>
<span data-ttu-id="798d8-115">A **set-AzDataFactoryV2** parancsmag adatfeldolgozót hoz létre a megadott erőforráscsoport-névvel és-hellyel.</span><span class="sxs-lookup"><span data-stu-id="798d8-115">The **Set-AzDataFactoryV2** cmdlet creates a data factory with the specified resource group name and location.</span></span>
<span data-ttu-id="798d8-116">Végezze el ezeket a műveleteket a következő sorrendben:-------hoz létre egy adatfeldolgozót.</span><span class="sxs-lookup"><span data-stu-id="798d8-116">Perform these operations in the following order: -- Create a data factory.</span></span>
<span data-ttu-id="798d8-117">– Kapcsolt szolgáltatások létrehozása.</span><span class="sxs-lookup"><span data-stu-id="798d8-117">-- Create linked services.</span></span>
<span data-ttu-id="798d8-118">– Adatkészletek létrehozása.</span><span class="sxs-lookup"><span data-stu-id="798d8-118">-- Create datasets.</span></span>
<span data-ttu-id="798d8-119">– Csővezeték létrehozása.</span><span class="sxs-lookup"><span data-stu-id="798d8-119">-- Create a pipeline.</span></span>

## <span data-ttu-id="798d8-120">Példák</span><span class="sxs-lookup"><span data-stu-id="798d8-120">EXAMPLES</span></span>

### <span data-ttu-id="798d8-121">Példa 1: adatfeldolgozó létrehozása</span><span class="sxs-lookup"><span data-stu-id="798d8-121">Example 1: Create a data factory</span></span>
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

### <span data-ttu-id="798d8-122">2. példa: a meglévő gyári objektum segítségével adatfeldolgozót hozhat létre a repó konfigurációs adataival.</span><span class="sxs-lookup"><span data-stu-id="798d8-122">Example 2: Create a data factory with repo configuration details using an existing factory object.</span></span>
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

<span data-ttu-id="798d8-123">Ez a parancs létrehoz egy WikiADF nevű adattárolót az ADF nevű erőforrás-csoportban, az EastUS helyen, az Azure DevOps adatforrás-vezérlési beállításaival.</span><span class="sxs-lookup"><span data-stu-id="798d8-123">This command creates a data factory named WikiADF in the resource group named ADF in the EastUS location with Azure DevOps source control configuration.</span></span>

### <span data-ttu-id="798d8-124">3. példa: adatgyár létrehozása a GitHub repo Configuration Details (új gyári objektum) segítségével.</span><span class="sxs-lookup"><span data-stu-id="798d8-124">Example 3: Create a data factory with GitHub repo configuration details using a new factory object.</span></span>
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

<span data-ttu-id="798d8-125">Ez a parancs létrehoz egy WikiADF nevű adattárolót az ADF nevű erőforrás-csoport EastUS helyéről a GitHub verziókövetés konfigurációjával..</span><span class="sxs-lookup"><span data-stu-id="798d8-125">This command creates a data factory named WikiADF in the resource group named ADF in the EastUS location with GitHub source control configuration..</span></span>

## <span data-ttu-id="798d8-126">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="798d8-126">PARAMETERS</span></span>

### <span data-ttu-id="798d8-127">-AccountName</span><span class="sxs-lookup"><span data-stu-id="798d8-127">-AccountName</span></span>
<span data-ttu-id="798d8-128">A repó-konfigurációhoz tartozó fióknév.</span><span class="sxs-lookup"><span data-stu-id="798d8-128">The account name for repo configuration.</span></span>

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

### <span data-ttu-id="798d8-129">-CollaborationBranch</span><span class="sxs-lookup"><span data-stu-id="798d8-129">-CollaborationBranch</span></span>
<span data-ttu-id="798d8-130">A repo-konfiguráció együttműködési ága.</span><span class="sxs-lookup"><span data-stu-id="798d8-130">The collaboration branch for repo configuration.</span></span>

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

### <span data-ttu-id="798d8-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="798d8-131">-DefaultProfile</span></span>
<span data-ttu-id="798d8-132">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="798d8-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="798d8-133">-Force</span><span class="sxs-lookup"><span data-stu-id="798d8-133">-Force</span></span>
<span data-ttu-id="798d8-134">A parancsmag futtatása megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="798d8-134">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="798d8-135">-HostName (állomásnév)</span><span class="sxs-lookup"><span data-stu-id="798d8-135">-HostName</span></span>
<span data-ttu-id="798d8-136">A GitHub repó-konfiguráció állomásnevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="798d8-136">The host name for GitHub repo configuration.</span></span>

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

### <span data-ttu-id="798d8-137">-InputObject</span><span class="sxs-lookup"><span data-stu-id="798d8-137">-InputObject</span></span>
<span data-ttu-id="798d8-138">Az Data Factory objektum.</span><span class="sxs-lookup"><span data-stu-id="798d8-138">The data factory object.</span></span>

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

### <span data-ttu-id="798d8-139">-LastCommitId</span><span class="sxs-lookup"><span data-stu-id="798d8-139">-LastCommitId</span></span>
<span data-ttu-id="798d8-140">A repo-konfiguráció utolsó véglegesítési azonosítója.</span><span class="sxs-lookup"><span data-stu-id="798d8-140">The last commit id for repo configuration.</span></span>

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

### <span data-ttu-id="798d8-141">-Hely</span><span class="sxs-lookup"><span data-stu-id="798d8-141">-Location</span></span>
<span data-ttu-id="798d8-142">Az adatfeldolgozó ebben a régióban jön létre.</span><span class="sxs-lookup"><span data-stu-id="798d8-142">The data factory is created in this region.</span></span>

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

### <span data-ttu-id="798d8-143">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="798d8-143">-Name</span></span>
<span data-ttu-id="798d8-144">Az adatgyári név.</span><span class="sxs-lookup"><span data-stu-id="798d8-144">The data factory name.</span></span>

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

### <span data-ttu-id="798d8-145">-Projektnév</span><span class="sxs-lookup"><span data-stu-id="798d8-145">-ProjectName</span></span>
<span data-ttu-id="798d8-146">A projekt neve Azure DevOps for repo Configuration.</span><span class="sxs-lookup"><span data-stu-id="798d8-146">The project name Azure DevOps for repo configuration.</span></span>

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

### <span data-ttu-id="798d8-147">-RepositoryName</span><span class="sxs-lookup"><span data-stu-id="798d8-147">-RepositoryName</span></span>
<span data-ttu-id="798d8-148">A repó-konfiguráció tárházának neve.</span><span class="sxs-lookup"><span data-stu-id="798d8-148">The repository name for repo configuration.</span></span>

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

### <span data-ttu-id="798d8-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="798d8-149">-ResourceGroupName</span></span>
<span data-ttu-id="798d8-150">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="798d8-150">The resource group name.</span></span>

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

### <span data-ttu-id="798d8-151">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="798d8-151">-ResourceId</span></span>
<span data-ttu-id="798d8-152">Az Azure Resource ID of v2 Data Factory.</span><span class="sxs-lookup"><span data-stu-id="798d8-152">The Azure resource ID of V2 data factory.</span></span>

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

### <span data-ttu-id="798d8-153">-RootFolder</span><span class="sxs-lookup"><span data-stu-id="798d8-153">-RootFolder</span></span>
<span data-ttu-id="798d8-154">A repó-konfiguráció gyökerének mappája.</span><span class="sxs-lookup"><span data-stu-id="798d8-154">The root folder for repo configuration.</span></span>

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

### <span data-ttu-id="798d8-155">-Címke</span><span class="sxs-lookup"><span data-stu-id="798d8-155">-Tag</span></span>
<span data-ttu-id="798d8-156">Az adatfeldolgozó címkéi.</span><span class="sxs-lookup"><span data-stu-id="798d8-156">The tags of the data factory.</span></span>

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

### <span data-ttu-id="798d8-157">-Bérlői azonosító megkeresése</span><span class="sxs-lookup"><span data-stu-id="798d8-157">-TenantId</span></span>
<span data-ttu-id="798d8-158">Az Azure DevOps repo Configuration (bérlői azonosító)</span><span class="sxs-lookup"><span data-stu-id="798d8-158">The tenant id for Azure DevOps repo configuration.</span></span>

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

### <span data-ttu-id="798d8-159">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="798d8-159">-Confirm</span></span>
<span data-ttu-id="798d8-160">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="798d8-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="798d8-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="798d8-161">-WhatIf</span></span>
<span data-ttu-id="798d8-162">Itt láthatja, hogy mi történik, ha a parancsmag fut, de nem futtatja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="798d8-162">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="798d8-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="798d8-163">CommonParameters</span></span>
<span data-ttu-id="798d8-164">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="798d8-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="798d8-165">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="798d8-165">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="798d8-166">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="798d8-166">INPUTS</span></span>

### <span data-ttu-id="798d8-167">System. String</span><span class="sxs-lookup"><span data-stu-id="798d8-167">System.String</span></span>

### <span data-ttu-id="798d8-168">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="798d8-168">System.Collections.Hashtable</span></span>

## <span data-ttu-id="798d8-169">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="798d8-169">OUTPUTS</span></span>

### <span data-ttu-id="798d8-170">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="798d8-170">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="798d8-171">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="798d8-171">NOTES</span></span>
<span data-ttu-id="798d8-172">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak</span><span class="sxs-lookup"><span data-stu-id="798d8-172">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="798d8-173">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="798d8-173">RELATED LINKS</span></span>

[<span data-ttu-id="798d8-174">Get-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="798d8-174">Get-AzDataFactoryV2</span></span>]()

[<span data-ttu-id="798d8-175">Remove-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="798d8-175">Remove-AzDataFactoryV2</span></span>]()
