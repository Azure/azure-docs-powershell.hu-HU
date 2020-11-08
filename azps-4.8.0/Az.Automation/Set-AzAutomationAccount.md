---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B1897EFC-0184-4A8B-B8E4-203CC8E3B179
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationAccount.md
ms.openlocfilehash: f32e9c0d76e88fba5475abb39595b0a6c4bea834
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183721"
---
# <span data-ttu-id="31d62-101">Set-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="31d62-101">Set-AzAutomationAccount</span></span>

## <span data-ttu-id="31d62-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="31d62-102">SYNOPSIS</span></span>
<span data-ttu-id="31d62-103">Automatizálási fiók módosítása</span><span class="sxs-lookup"><span data-stu-id="31d62-103">Modifies an Automation account.</span></span>

## <span data-ttu-id="31d62-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="31d62-104">SYNTAX</span></span>

```
Set-AzAutomationAccount [-ResourceGroupName] <String> [-Name] <String> [-Plan <String>] [-Tags <IDictionary>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="31d62-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="31d62-105">DESCRIPTION</span></span>
<span data-ttu-id="31d62-106">A **set-AzAutomationAccount** parancsmag az Azure automatizálási fiókját módosítja.</span><span class="sxs-lookup"><span data-stu-id="31d62-106">The **Set-AzAutomationAccount** cmdlet modifies an Azure Automation account.</span></span>
<span data-ttu-id="31d62-107">Az automatizálási fiókokról további információt az New-AzAutomationAccount parancsmag című témakörben találhat.</span><span class="sxs-lookup"><span data-stu-id="31d62-107">For more information about Automation accounts, see the New-AzAutomationAccount cmdlet.</span></span>

## <span data-ttu-id="31d62-108">Példák</span><span class="sxs-lookup"><span data-stu-id="31d62-108">EXAMPLES</span></span>

### <span data-ttu-id="31d62-109">Példa 1: automatizálási fiók címkékének beállítása</span><span class="sxs-lookup"><span data-stu-id="31d62-109">Example 1: Set the tags for an Automation account</span></span>
```
PS C:\>$Tags = @{"tag01"="value01";"tag02"="value02"}
PS C:\> Set-AzAutomationAccount -Name "AutomationAccount01" -ResourceGroupName "ResourceGroup01" -Tags $Tags
```

<span data-ttu-id="31d62-110">Az első parancs két kulcs/érték párokat rendel a $Tags változóhoz.</span><span class="sxs-lookup"><span data-stu-id="31d62-110">The first command assigns two key/value pairs to the $Tags variable.</span></span>
<span data-ttu-id="31d62-111">A második parancs a AutomationAccount01 nevű automatizálási fiókhoz $Tags címkéket állít be.</span><span class="sxs-lookup"><span data-stu-id="31d62-111">The second command sets tags in $Tags for the Automation account named AutomationAccount01.</span></span>

### <span data-ttu-id="31d62-112">2. példa: az automatizálási fiók tervének módosítása</span><span class="sxs-lookup"><span data-stu-id="31d62-112">Example 2: Change the plan for an Automation account</span></span>
```
PS C:\>Set-AzAutomationAccount -Name "AutomationAccount01" -ResourceGroupName "ResourceGroup01" -Plan Basic
```

<span data-ttu-id="31d62-113">Ez a parancs a AutomationAccount01 nevű automatizálási fiók esetében módosítja az alaptervet.</span><span class="sxs-lookup"><span data-stu-id="31d62-113">This command changes the plan to Basic for the Automation account named AutomationAccount01.</span></span>

## <span data-ttu-id="31d62-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="31d62-114">PARAMETERS</span></span>

### <span data-ttu-id="31d62-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31d62-115">-DefaultProfile</span></span>
<span data-ttu-id="31d62-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="31d62-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="31d62-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="31d62-117">-Name</span></span>
<span data-ttu-id="31d62-118">A parancsmag által módosított automatizálási fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="31d62-118">Specifies the name of the Automation account that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="31d62-119">-Terv</span><span class="sxs-lookup"><span data-stu-id="31d62-119">-Plan</span></span>
<span data-ttu-id="31d62-120">Az automatizálási fiók tervét adja meg.</span><span class="sxs-lookup"><span data-stu-id="31d62-120">Specifies the plan for the Automation account.</span></span>
<span data-ttu-id="31d62-121">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="31d62-121">Valid values are:</span></span>
- <span data-ttu-id="31d62-122">Egyszerű</span><span class="sxs-lookup"><span data-stu-id="31d62-122">Basic</span></span>
- <span data-ttu-id="31d62-123">Ingyenes</span><span class="sxs-lookup"><span data-stu-id="31d62-123">Free</span></span>

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

### <span data-ttu-id="31d62-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31d62-124">-ResourceGroupName</span></span>
<span data-ttu-id="31d62-125">Annak az erőforrás-csoportnak a nevét adja meg, amely a parancsmag által módosított automatizálási fiókot tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="31d62-125">Specifies the name of a resource group that contains the Automation account that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="31d62-126">-Címkék</span><span class="sxs-lookup"><span data-stu-id="31d62-126">-Tags</span></span>
<span data-ttu-id="31d62-127">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="31d62-127">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="31d62-128">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="31d62-128">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="31d62-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31d62-129">CommonParameters</span></span>
<span data-ttu-id="31d62-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="31d62-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31d62-131">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31d62-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31d62-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="31d62-132">INPUTS</span></span>

### <span data-ttu-id="31d62-133">System. String</span><span class="sxs-lookup"><span data-stu-id="31d62-133">System.String</span></span>

### <span data-ttu-id="31d62-134">System. Collections. IDictionary</span><span class="sxs-lookup"><span data-stu-id="31d62-134">System.Collections.IDictionary</span></span>

## <span data-ttu-id="31d62-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="31d62-135">OUTPUTS</span></span>

### <span data-ttu-id="31d62-136">Microsoft. Azure. Command. Automation. Model. AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="31d62-136">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="31d62-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="31d62-137">NOTES</span></span>

## <span data-ttu-id="31d62-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="31d62-138">RELATED LINKS</span></span>

[<span data-ttu-id="31d62-139">Get-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="31d62-139">Get-AzAutomationAccount</span></span>](./Get-AzAutomationAccount.md)

[<span data-ttu-id="31d62-140">Új – AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="31d62-140">New-AzAutomationAccount</span></span>](./New-AzAutomationAccount.md)

[<span data-ttu-id="31d62-141">Remove-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="31d62-141">Remove-AzAutomationAccount</span></span>](./Remove-AzAutomationAccount.md)
