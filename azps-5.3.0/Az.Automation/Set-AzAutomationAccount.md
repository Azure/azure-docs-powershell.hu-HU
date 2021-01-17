---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B1897EFC-0184-4A8B-B8E4-203CC8E3B179
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationAccount.md
ms.openlocfilehash: f32e9c0d76e88fba5475abb39595b0a6c4bea834
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98478505"
---
# <span data-ttu-id="fbe20-101">Set-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="fbe20-101">Set-AzAutomationAccount</span></span>

## <span data-ttu-id="fbe20-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fbe20-102">SYNOPSIS</span></span>
<span data-ttu-id="fbe20-103">Módosítja az Automatizálási fiókot.</span><span class="sxs-lookup"><span data-stu-id="fbe20-103">Modifies an Automation account.</span></span>

## <span data-ttu-id="fbe20-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="fbe20-104">SYNTAX</span></span>

```
Set-AzAutomationAccount [-ResourceGroupName] <String> [-Name] <String> [-Plan <String>] [-Tags <IDictionary>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fbe20-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="fbe20-105">DESCRIPTION</span></span>
<span data-ttu-id="fbe20-106">A **Set-AzAutomationAccount** parancsmag módosítja az Azure Automation-fiókot.</span><span class="sxs-lookup"><span data-stu-id="fbe20-106">The **Set-AzAutomationAccount** cmdlet modifies an Azure Automation account.</span></span>
<span data-ttu-id="fbe20-107">Az automatizálási fiókokról további információt a New-AzAutomationAccount parancsmagban.</span><span class="sxs-lookup"><span data-stu-id="fbe20-107">For more information about Automation accounts, see the New-AzAutomationAccount cmdlet.</span></span>

## <span data-ttu-id="fbe20-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="fbe20-108">EXAMPLES</span></span>

### <span data-ttu-id="fbe20-109">1. példa: Automatizálási fiók címkéinek beállítása</span><span class="sxs-lookup"><span data-stu-id="fbe20-109">Example 1: Set the tags for an Automation account</span></span>
```
PS C:\>$Tags = @{"tag01"="value01";"tag02"="value02"}
PS C:\> Set-AzAutomationAccount -Name "AutomationAccount01" -ResourceGroupName "ResourceGroup01" -Tags $Tags
```

<span data-ttu-id="fbe20-110">Az első parancs két kulcs-érték párt rendel a $Tags változóhoz.</span><span class="sxs-lookup"><span data-stu-id="fbe20-110">The first command assigns two key/value pairs to the $Tags variable.</span></span>
<span data-ttu-id="fbe20-111">A második parancs az AutomationAccount01 nevű $Tags-fiók címkéit állítja be a $Tags.</span><span class="sxs-lookup"><span data-stu-id="fbe20-111">The second command sets tags in $Tags for the Automation account named AutomationAccount01.</span></span>

### <span data-ttu-id="fbe20-112">2. példa: Automatizálási fiók tervének módosítása</span><span class="sxs-lookup"><span data-stu-id="fbe20-112">Example 2: Change the plan for an Automation account</span></span>
```
PS C:\>Set-AzAutomationAccount -Name "AutomationAccount01" -ResourceGroupName "ResourceGroup01" -Plan Basic
```

<span data-ttu-id="fbe20-113">Ez a parancs az AutomationAccount01 nevű Automatizálási fiók alapszintű csomagjára módosítja a tervet.</span><span class="sxs-lookup"><span data-stu-id="fbe20-113">This command changes the plan to Basic for the Automation account named AutomationAccount01.</span></span>

## <span data-ttu-id="fbe20-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fbe20-114">PARAMETERS</span></span>

### <span data-ttu-id="fbe20-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbe20-115">-DefaultProfile</span></span>
<span data-ttu-id="fbe20-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="fbe20-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fbe20-117">-Name</span><span class="sxs-lookup"><span data-stu-id="fbe20-117">-Name</span></span>
<span data-ttu-id="fbe20-118">Annak az automatizálási fióknak a nevét adja meg, amit ez a parancsmag módosít.</span><span class="sxs-lookup"><span data-stu-id="fbe20-118">Specifies the name of the Automation account that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AutomationAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbe20-119">-Plan</span><span class="sxs-lookup"><span data-stu-id="fbe20-119">-Plan</span></span>
<span data-ttu-id="fbe20-120">Az Automatizálási fiók csomagját határozza meg.</span><span class="sxs-lookup"><span data-stu-id="fbe20-120">Specifies the plan for the Automation account.</span></span>
<span data-ttu-id="fbe20-121">Érvényes értékek:</span><span class="sxs-lookup"><span data-stu-id="fbe20-121">Valid values are:</span></span>
- <span data-ttu-id="fbe20-122">Alapszintű</span><span class="sxs-lookup"><span data-stu-id="fbe20-122">Basic</span></span>
- <span data-ttu-id="fbe20-123">Ingyenes</span><span class="sxs-lookup"><span data-stu-id="fbe20-123">Free</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Free, Basic

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbe20-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbe20-124">-ResourceGroupName</span></span>
<span data-ttu-id="fbe20-125">Annak az erőforráscsoportnak a nevét adja meg, amely a parancsmag által módosított Automatizálási fiókot tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="fbe20-125">Specifies the name of a resource group that contains the Automation account that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="fbe20-126">-Címkék</span><span class="sxs-lookup"><span data-stu-id="fbe20-126">-Tags</span></span>
<span data-ttu-id="fbe20-127">Kulcsérték-párok kivonattábla formájában.</span><span class="sxs-lookup"><span data-stu-id="fbe20-127">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="fbe20-128">Például: @{key0="érték0";key1=$null;key2="érték2"}</span><span class="sxs-lookup"><span data-stu-id="fbe20-128">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbe20-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbe20-129">CommonParameters</span></span>
<span data-ttu-id="fbe20-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fbe20-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbe20-131">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fbe20-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbe20-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fbe20-132">INPUTS</span></span>

### <span data-ttu-id="fbe20-133">System.String</span><span class="sxs-lookup"><span data-stu-id="fbe20-133">System.String</span></span>

### <span data-ttu-id="fbe20-134">System.Collections.IDictionary</span><span class="sxs-lookup"><span data-stu-id="fbe20-134">System.Collections.IDictionary</span></span>

## <span data-ttu-id="fbe20-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fbe20-135">OUTPUTS</span></span>

### <span data-ttu-id="fbe20-136">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="fbe20-136">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="fbe20-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="fbe20-137">NOTES</span></span>

## <span data-ttu-id="fbe20-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fbe20-138">RELATED LINKS</span></span>

[<span data-ttu-id="fbe20-139">Get-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="fbe20-139">Get-AzAutomationAccount</span></span>](./Get-AzAutomationAccount.md)

[<span data-ttu-id="fbe20-140">New-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="fbe20-140">New-AzAutomationAccount</span></span>](./New-AzAutomationAccount.md)

[<span data-ttu-id="fbe20-141">Remove-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="fbe20-141">Remove-AzAutomationAccount</span></span>](./Remove-AzAutomationAccount.md)
