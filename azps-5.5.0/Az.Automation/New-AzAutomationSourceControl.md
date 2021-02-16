---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationsourcecontrol
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationSourceControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationSourceControl.md
ms.openlocfilehash: 17d1c7c94726543aa30a032423576c8a7dcb6fcc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100168242"
---
# <span data-ttu-id="d8155-101">New-AzAutomationSourceControl</span><span class="sxs-lookup"><span data-stu-id="d8155-101">New-AzAutomationSourceControl</span></span>

## <span data-ttu-id="d8155-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8155-102">SYNOPSIS</span></span>
<span data-ttu-id="d8155-103">Létrehoz egy automatizálási forrásvezérlőt.</span><span class="sxs-lookup"><span data-stu-id="d8155-103">Creates an A Automation source control.</span></span>

## <span data-ttu-id="d8155-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d8155-104">SYNTAX</span></span>

```
New-AzAutomationSourceControl -Name <String> -RepoUrl <Uri> -SourceType <String> -AccessToken <SecureString>
 -FolderPath <String> [-Branch <String>] [-Description <String>] [-EnableAutoSync] [-DoNotPublishRunbook]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8155-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d8155-105">DESCRIPTION</span></span>
<span data-ttu-id="d8155-106">A New-AzAutomationSourceControl parancsmag létrehoz egy konfigurációt, amely összekapcsolja az Azure Automation-fiókomat a VSTS TFVC, a VSTS Git vagy a GitHub használatával.</span><span class="sxs-lookup"><span data-stu-id="d8155-106">The New-AzAutomationSourceControl cmdlet creates a configuration to link my Azure Automation account with my VSTS TFVC, VSTS Git or GitHub.</span></span>

## <span data-ttu-id="d8155-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d8155-107">EXAMPLES</span></span>

### <span data-ttu-id="d8155-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="d8155-108">Example 1</span></span>
<span data-ttu-id="d8155-109">Létrehozhat egy forrásvezérlő-konfigurációt, hogy összekapcsolja az Azure Automation-fiókomat a VSTS TFVC-projekttel.</span><span class="sxs-lookup"><span data-stu-id="d8155-109">Create a source control configuration to link my Azure Automation account with my VSTS TFVC project.</span></span> <span data-ttu-id="d8155-110">A TFVC-projekteknek nincs ága, ezért az Ág paraméter nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="d8155-110">TFVC projects do not have branches, and therefore, the Branch parameter is not specified.</span></span>

```powershell
PS C:\> # VSTS Personal access token
PS C:\> $token = "vppmrabbs65axamofglyo66rjg6reddaa7xxgvaddd5555aaaaddxzbmma"
PS C:\> $accessToken = ConvertTo-SecureString -String $token -AsPlainText -Force 
PS C:\> New-AzAutomationSourceControl -ResourceGroupName "rg1" `
                                           -AutomationAccountName "devAccount" `
                                           -Name  "VSTSNative" `
                                           -RepoUrl "https://contoso.visualstudio.com/ContosoProduction/_versionControl" `
                                           -SourceType "VsoTfvc" `
                                           -FolderPath "/Runbooks" `
                                           -AccessToken $accessToken

Name        SourceType Branch FolderPath AutoSync PublishRunbook RepoUrl
----        ---------- ------ ---------- -------- -------------- -------
VSTSNative  VsoTfvc            /Runbooks True     True           https://contoso.visualstudio.com/ContosoProduc...
```

### <span data-ttu-id="d8155-111">2. példa</span><span class="sxs-lookup"><span data-stu-id="d8155-111">Example 2</span></span>
<span data-ttu-id="d8155-112">Létrehozhat egy forrásvezérlő-konfigurációt, amely összekapcsolja az Azure Automation-fiókomat a VSTS Git-projekttel.</span><span class="sxs-lookup"><span data-stu-id="d8155-112">Create a source control configuration to link my Azure Automation account with my VSTS Git project.</span></span>


```powershell
PS C:\> # VSTS Personal access token
PS C:\> $token = "vppmrabbs65axamofglyo66rjg6reddaa7xxgvaddd5555aaaaddxzbmma"
PS C:\> $accessToken = ConvertTo-SecureString -String $token -AsPlainText -Force 
PS C:\> New-AzAutomationSourceControl -ResourceGroupName "rg1" `
                                           -AutomationAccountName "devAccount" `
                                           -Name  "VSTSGit" `
                                           -RepoUrl "https://contoso.visualstudio.com/_git/Finance" `
                                           -SourceType "VsoGit" `
                                           -Branch "Development" `
                                           -FolderPath "/" `
                                           -AccessToken $accessToken

Name    SourceType Branch      FolderPath AutoSync PublishRunbook RepoUrl
----    ---------- ------      ---------- -------- -------------- -------
VSTSGit VsoGit     Development /          True     True           https://contoso.visualstudio.com/_git/Finan...
```

### <span data-ttu-id="d8155-113">3. példa</span><span class="sxs-lookup"><span data-stu-id="d8155-113">Example 3</span></span>
<span data-ttu-id="d8155-114">Létrehozhat egy forrásvezérlő-konfigurációt, hogy összekapcsolja az Azure Automation-fiókomat a GitHub-projekttel.</span><span class="sxs-lookup"><span data-stu-id="d8155-114">Create a source control configuration to link my Azure Automation account with my GitHub project.</span></span>


```powershell
PS C:\> # GitHub access token
PS C:\> $token = "68b08011223aac8bdd3388913a44rrsaa84fdf"
PS C:\> $accessToken = ConvertTo-SecureString -String $token -AsPlainText -Force 
PS C:\> New-AzAutomationSourceControl -ResourceGroupName "rg1" `
                                           -AutomationAccountName "devAccount" `
                                           -Name  "GitHub1" `
                                           -RepoUrl "https://github.com/Contoso/TestSourceControl.git" `
                                           -SourceType "GitHub" `
                                           -Branch "master" `
                                           -FolderPath "/Runbooks" `
                                           -AccessToken $accessToken

Name    SourceType Branch FolderPath AutoSync PublishRunbook RepoUrl
----    ---------- ------ ---------- -------- -------------- -------
GitHub1 GitHub     master /Runbooks  True     True           https://github.com/Contoso/TestSourceControl...
```

## <span data-ttu-id="d8155-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d8155-115">PARAMETERS</span></span>

### <span data-ttu-id="d8155-116">-AccessToken</span><span class="sxs-lookup"><span data-stu-id="d8155-116">-AccessToken</span></span>
<span data-ttu-id="d8155-117">A forrásvezérlő hozzáférési jogkivonata.</span><span class="sxs-lookup"><span data-stu-id="d8155-117">The source control access token.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8155-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d8155-118">-AutomationAccountName</span></span>
<span data-ttu-id="d8155-119">Az automatizálási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="d8155-119">The automation account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8155-120">-Branch</span><span class="sxs-lookup"><span data-stu-id="d8155-120">-Branch</span></span>
<span data-ttu-id="d8155-121">A forrásvezérlő ág.</span><span class="sxs-lookup"><span data-stu-id="d8155-121">The source control branch.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8155-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8155-122">-DefaultProfile</span></span>
<span data-ttu-id="d8155-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d8155-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8155-124">-Leírás</span><span class="sxs-lookup"><span data-stu-id="d8155-124">-Description</span></span>
<span data-ttu-id="d8155-125">A forrásvezérlő leírása.</span><span class="sxs-lookup"><span data-stu-id="d8155-125">The source control description.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8155-126">-DoNotPublishRunbook</span><span class="sxs-lookup"><span data-stu-id="d8155-126">-DoNotPublishRunbook</span></span>
<span data-ttu-id="d8155-127">A forrásvezérlő PublishRunbook tulajdonsága.</span><span class="sxs-lookup"><span data-stu-id="d8155-127">The publishRunbook property of the source control.</span></span>
<span data-ttu-id="d8155-128">Ha a DoNotPublishRunbook be van állítva, az azt jelenti, hogy a felhasználói runbookok "Piszkozatként" lesznek importálva.</span><span class="sxs-lookup"><span data-stu-id="d8155-128">If DoNotPublishRunbook is set, this means that user runbooks will be imported as 'Draft'.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8155-129">-EnableAutoSync</span><span class="sxs-lookup"><span data-stu-id="d8155-129">-EnableAutoSync</span></span>
<span data-ttu-id="d8155-130">A forrásvezérlő AutoSync tulajdonsága.</span><span class="sxs-lookup"><span data-stu-id="d8155-130">The autoSync property for the source control.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8155-131">-FolderPath</span><span class="sxs-lookup"><span data-stu-id="d8155-131">-FolderPath</span></span>
<span data-ttu-id="d8155-132">A forrásvezérlő mappa elérési útja.</span><span class="sxs-lookup"><span data-stu-id="d8155-132">The source control folder path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8155-133">-Name</span><span class="sxs-lookup"><span data-stu-id="d8155-133">-Name</span></span>
<span data-ttu-id="d8155-134">A forrásvezérlő neve.</span><span class="sxs-lookup"><span data-stu-id="d8155-134">The source control name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8155-135">-RepoUrl</span><span class="sxs-lookup"><span data-stu-id="d8155-135">-RepoUrl</span></span>
<span data-ttu-id="d8155-136">A forrásvezérlő-repo URL-címe.</span><span class="sxs-lookup"><span data-stu-id="d8155-136">The source control repo url.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8155-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8155-137">-ResourceGroupName</span></span>
<span data-ttu-id="d8155-138">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="d8155-138">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8155-139">-SourceType</span><span class="sxs-lookup"><span data-stu-id="d8155-139">-SourceType</span></span>
<span data-ttu-id="d8155-140">A forrásvezérlő típusa.</span><span class="sxs-lookup"><span data-stu-id="d8155-140">The source control type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: GitHub, VsoGit, VsoTfvc

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8155-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d8155-141">-Confirm</span></span>
<span data-ttu-id="d8155-142">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d8155-142">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8155-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8155-143">-WhatIf</span></span>
<span data-ttu-id="d8155-144">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d8155-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8155-145">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d8155-145">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8155-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8155-146">CommonParameters</span></span>
<span data-ttu-id="d8155-147">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8155-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8155-148">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8155-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8155-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d8155-149">INPUTS</span></span>

### <span data-ttu-id="d8155-150">System.String</span><span class="sxs-lookup"><span data-stu-id="d8155-150">System.String</span></span>

## <span data-ttu-id="d8155-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d8155-151">OUTPUTS</span></span>

### <span data-ttu-id="d8155-152">Microsoft.Azure.Commands.Automation.Model.SourceControl</span><span class="sxs-lookup"><span data-stu-id="d8155-152">Microsoft.Azure.Commands.Automation.Model.SourceControl</span></span>

## <span data-ttu-id="d8155-153">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d8155-153">NOTES</span></span>

## <span data-ttu-id="d8155-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d8155-154">RELATED LINKS</span></span>
