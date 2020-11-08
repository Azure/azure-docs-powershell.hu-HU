---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationsourcecontrol
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSourceControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSourceControl.md
ms.openlocfilehash: 42472efdde4ccf96f12a0617d9a86175eed13d1c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182644"
---
# <span data-ttu-id="13d44-101">Get-AzAutomationSourceControl</span><span class="sxs-lookup"><span data-stu-id="13d44-101">Get-AzAutomationSourceControl</span></span>

## <span data-ttu-id="13d44-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="13d44-102">SYNOPSIS</span></span>
<span data-ttu-id="13d44-103">Beolvassa az Azure automatizálási vezérlők listáját.</span><span class="sxs-lookup"><span data-stu-id="13d44-103">Gets a list of Azure Automation source controls.</span></span>

## <span data-ttu-id="13d44-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="13d44-104">SYNTAX</span></span>

### <span data-ttu-id="13d44-105">ByAll (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="13d44-105">ByAll (Default)</span></span>
```
Get-AzAutomationSourceControl [-SourceType <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="13d44-106">ByName</span><span class="sxs-lookup"><span data-stu-id="13d44-106">ByName</span></span>
```
Get-AzAutomationSourceControl -Name <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="13d44-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="13d44-107">DESCRIPTION</span></span>
<span data-ttu-id="13d44-108">Az Get-AzAutomationSourceControl parancsmag automatizálási adatforrás-vezérlőket kap.</span><span class="sxs-lookup"><span data-stu-id="13d44-108">The Get-AzAutomationSourceControl cmdlet gets Automation source controls.</span></span>
<span data-ttu-id="13d44-109">Ha egy konkrét forrás vezérlőt szeretne beszerezni, adja meg a nevét.</span><span class="sxs-lookup"><span data-stu-id="13d44-109">To get a specific source control, specify its name.</span></span>

## <span data-ttu-id="13d44-110">Példák</span><span class="sxs-lookup"><span data-stu-id="13d44-110">EXAMPLES</span></span>

### <span data-ttu-id="13d44-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="13d44-111">Example 1</span></span>
<span data-ttu-id="13d44-112">Ez a parancs egy VSTSNative nevű automatizálási vezérlőt kap a devAccount nevű fiókban.</span><span class="sxs-lookup"><span data-stu-id="13d44-112">This command gets an Automation source control named VSTSNative in the account named devAccount.</span></span>


```powershell
PS C:\> Get-AzAutomationSourceControl -ResourceGroupName "rg1" `
                                           -AutomationAccountName "devAccount" `
                                           -Name "VSTSNative" 


Name            SourceType Branch FolderPath  AutoSync PublishRunbook RepoUrl
----            ---------- ------ ----------  -------- -------------- -------
VSTSNative      VsoTfvc           /MyRunbooks False    True           https://contoso.visualstudio.com/_git/Fin...
```

## <span data-ttu-id="13d44-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="13d44-113">PARAMETERS</span></span>

### <span data-ttu-id="13d44-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="13d44-114">-AutomationAccountName</span></span>
<span data-ttu-id="13d44-115">Az automatizálási fiók neve.</span><span class="sxs-lookup"><span data-stu-id="13d44-115">The automation account name.</span></span>

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

### <span data-ttu-id="13d44-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13d44-116">-DefaultProfile</span></span>
<span data-ttu-id="13d44-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="13d44-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13d44-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="13d44-118">-Name</span></span>
<span data-ttu-id="13d44-119">A forrás vezérlő neve.</span><span class="sxs-lookup"><span data-stu-id="13d44-119">The source control name.</span></span>

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

### <span data-ttu-id="13d44-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13d44-120">-ResourceGroupName</span></span>
<span data-ttu-id="13d44-121">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="13d44-121">The resource group name.</span></span>

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

### <span data-ttu-id="13d44-122">-SourceType</span><span class="sxs-lookup"><span data-stu-id="13d44-122">-SourceType</span></span>
<span data-ttu-id="13d44-123">A forrás vezérlőelem típusa.</span><span class="sxs-lookup"><span data-stu-id="13d44-123">The source control type.</span></span>

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

### <span data-ttu-id="13d44-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13d44-124">CommonParameters</span></span>
<span data-ttu-id="13d44-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="13d44-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13d44-126">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13d44-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13d44-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="13d44-127">INPUTS</span></span>

### <span data-ttu-id="13d44-128">System. String</span><span class="sxs-lookup"><span data-stu-id="13d44-128">System.String</span></span>

## <span data-ttu-id="13d44-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="13d44-129">OUTPUTS</span></span>

### <span data-ttu-id="13d44-130">Microsoft. Azure. Command. Automation. Model. SourceControl</span><span class="sxs-lookup"><span data-stu-id="13d44-130">Microsoft.Azure.Commands.Automation.Model.SourceControl</span></span>

## <span data-ttu-id="13d44-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="13d44-131">NOTES</span></span>

## <span data-ttu-id="13d44-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="13d44-132">RELATED LINKS</span></span>
