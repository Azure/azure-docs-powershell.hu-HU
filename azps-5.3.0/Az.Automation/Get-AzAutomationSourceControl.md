---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationsourcecontrol
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSourceControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSourceControl.md
ms.openlocfilehash: 42472efdde4ccf96f12a0617d9a86175eed13d1c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98478666"
---
# <span data-ttu-id="32b20-101">Get-AzAutomationSourceControl</span><span class="sxs-lookup"><span data-stu-id="32b20-101">Get-AzAutomationSourceControl</span></span>

## <span data-ttu-id="32b20-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="32b20-102">SYNOPSIS</span></span>
<span data-ttu-id="32b20-103">Az Azure Automation forrásvezérlőinek listáját tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="32b20-103">Gets a list of Azure Automation source controls.</span></span>

## <span data-ttu-id="32b20-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="32b20-104">SYNTAX</span></span>

### <span data-ttu-id="32b20-105">ByAll (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="32b20-105">ByAll (Default)</span></span>
```
Get-AzAutomationSourceControl [-SourceType <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="32b20-106">ByName</span><span class="sxs-lookup"><span data-stu-id="32b20-106">ByName</span></span>
```
Get-AzAutomationSourceControl -Name <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="32b20-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="32b20-107">DESCRIPTION</span></span>
<span data-ttu-id="32b20-108">A Get-AzAutomationSourceControl parancsmag automatizálási forrásvezérlőket kap.</span><span class="sxs-lookup"><span data-stu-id="32b20-108">The Get-AzAutomationSourceControl cmdlet gets Automation source controls.</span></span>
<span data-ttu-id="32b20-109">Ha egy adott forrásvezérlőt is be kell szereznie, adja meg a nevét.</span><span class="sxs-lookup"><span data-stu-id="32b20-109">To get a specific source control, specify its name.</span></span>

## <span data-ttu-id="32b20-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="32b20-110">EXAMPLES</span></span>

### <span data-ttu-id="32b20-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="32b20-111">Example 1</span></span>
<span data-ttu-id="32b20-112">Ez a parancs egy VSTSNative nevű automatizálási forrásvezérlőt kap a devAccount nevű fiókban.</span><span class="sxs-lookup"><span data-stu-id="32b20-112">This command gets an Automation source control named VSTSNative in the account named devAccount.</span></span>


```powershell
PS C:\> Get-AzAutomationSourceControl -ResourceGroupName "rg1" `
                                           -AutomationAccountName "devAccount" `
                                           -Name "VSTSNative" 


Name            SourceType Branch FolderPath  AutoSync PublishRunbook RepoUrl
----            ---------- ------ ----------  -------- -------------- -------
VSTSNative      VsoTfvc           /MyRunbooks False    True           https://contoso.visualstudio.com/_git/Fin...
```

## <span data-ttu-id="32b20-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="32b20-113">PARAMETERS</span></span>

### <span data-ttu-id="32b20-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="32b20-114">-AutomationAccountName</span></span>
<span data-ttu-id="32b20-115">Az automatizálási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="32b20-115">The automation account name.</span></span>

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

### <span data-ttu-id="32b20-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32b20-116">-DefaultProfile</span></span>
<span data-ttu-id="32b20-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="32b20-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="32b20-118">-Name</span><span class="sxs-lookup"><span data-stu-id="32b20-118">-Name</span></span>
<span data-ttu-id="32b20-119">A forrásvezérlő neve.</span><span class="sxs-lookup"><span data-stu-id="32b20-119">The source control name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32b20-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32b20-120">-ResourceGroupName</span></span>
<span data-ttu-id="32b20-121">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="32b20-121">The resource group name.</span></span>

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

### <span data-ttu-id="32b20-122">-SourceType</span><span class="sxs-lookup"><span data-stu-id="32b20-122">-SourceType</span></span>
<span data-ttu-id="32b20-123">A forrásvezérlő típusa.</span><span class="sxs-lookup"><span data-stu-id="32b20-123">The source control type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAll
Aliases:
Accepted values: GitHub, VsoGit, VsoTfvc

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32b20-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32b20-124">CommonParameters</span></span>
<span data-ttu-id="32b20-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32b20-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32b20-126">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32b20-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32b20-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="32b20-127">INPUTS</span></span>

### <span data-ttu-id="32b20-128">System.String</span><span class="sxs-lookup"><span data-stu-id="32b20-128">System.String</span></span>

## <span data-ttu-id="32b20-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="32b20-129">OUTPUTS</span></span>

### <span data-ttu-id="32b20-130">Microsoft.Azure.Commands.Automation.Model.SourceControl</span><span class="sxs-lookup"><span data-stu-id="32b20-130">Microsoft.Azure.Commands.Automation.Model.SourceControl</span></span>

## <span data-ttu-id="32b20-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="32b20-131">NOTES</span></span>

## <span data-ttu-id="32b20-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="32b20-132">RELATED LINKS</span></span>
