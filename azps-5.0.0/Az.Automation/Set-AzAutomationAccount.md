---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B1897EFC-0184-4A8B-B8E4-203CC8E3B179
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationAccount.md
ms.openlocfilehash: f32e9c0d76e88fba5475abb39595b0a6c4bea834
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301607"
---
# <span data-ttu-id="cb86a-101">Set-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="cb86a-101">Set-AzAutomationAccount</span></span>

## <span data-ttu-id="cb86a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cb86a-102">SYNOPSIS</span></span>
<span data-ttu-id="cb86a-103">Automatizálási fiók módosítása</span><span class="sxs-lookup"><span data-stu-id="cb86a-103">Modifies an Automation account.</span></span>

## <span data-ttu-id="cb86a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cb86a-104">SYNTAX</span></span>

```
Set-AzAutomationAccount [-ResourceGroupName] <String> [-Name] <String> [-Plan <String>] [-Tags <IDictionary>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cb86a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="cb86a-105">DESCRIPTION</span></span>
<span data-ttu-id="cb86a-106">A **set-AzAutomationAccount** parancsmag az Azure automatizálási fiókját módosítja.</span><span class="sxs-lookup"><span data-stu-id="cb86a-106">The **Set-AzAutomationAccount** cmdlet modifies an Azure Automation account.</span></span>
<span data-ttu-id="cb86a-107">Az automatizálási fiókokról további információt az New-AzAutomationAccount parancsmag című témakörben találhat.</span><span class="sxs-lookup"><span data-stu-id="cb86a-107">For more information about Automation accounts, see the New-AzAutomationAccount cmdlet.</span></span>

## <span data-ttu-id="cb86a-108">Példák</span><span class="sxs-lookup"><span data-stu-id="cb86a-108">EXAMPLES</span></span>

### <span data-ttu-id="cb86a-109">Példa 1: automatizálási fiók címkékének beállítása</span><span class="sxs-lookup"><span data-stu-id="cb86a-109">Example 1: Set the tags for an Automation account</span></span>
```
PS C:\>$Tags = @{"tag01"="value01";"tag02"="value02"}
PS C:\> Set-AzAutomationAccount -Name "AutomationAccount01" -ResourceGroupName "ResourceGroup01" -Tags $Tags
```

<span data-ttu-id="cb86a-110">Az első parancs két kulcs/érték párokat rendel a $Tags változóhoz.</span><span class="sxs-lookup"><span data-stu-id="cb86a-110">The first command assigns two key/value pairs to the $Tags variable.</span></span>
<span data-ttu-id="cb86a-111">A második parancs a AutomationAccount01 nevű automatizálási fiókhoz $Tags címkéket állít be.</span><span class="sxs-lookup"><span data-stu-id="cb86a-111">The second command sets tags in $Tags for the Automation account named AutomationAccount01.</span></span>

### <span data-ttu-id="cb86a-112">2. példa: az automatizálási fiók tervének módosítása</span><span class="sxs-lookup"><span data-stu-id="cb86a-112">Example 2: Change the plan for an Automation account</span></span>
```
PS C:\>Set-AzAutomationAccount -Name "AutomationAccount01" -ResourceGroupName "ResourceGroup01" -Plan Basic
```

<span data-ttu-id="cb86a-113">Ez a parancs a AutomationAccount01 nevű automatizálási fiók esetében módosítja az alaptervet.</span><span class="sxs-lookup"><span data-stu-id="cb86a-113">This command changes the plan to Basic for the Automation account named AutomationAccount01.</span></span>

## <span data-ttu-id="cb86a-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cb86a-114">PARAMETERS</span></span>

### <span data-ttu-id="cb86a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb86a-115">-DefaultProfile</span></span>
<span data-ttu-id="cb86a-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="cb86a-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cb86a-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="cb86a-117">-Name</span></span>
<span data-ttu-id="cb86a-118">A parancsmag által módosított automatizálási fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cb86a-118">Specifies the name of the Automation account that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="cb86a-119">-Terv</span><span class="sxs-lookup"><span data-stu-id="cb86a-119">-Plan</span></span>
<span data-ttu-id="cb86a-120">Az automatizálási fiók tervét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cb86a-120">Specifies the plan for the Automation account.</span></span>
<span data-ttu-id="cb86a-121">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="cb86a-121">Valid values are:</span></span>
- <span data-ttu-id="cb86a-122">Egyszerű</span><span class="sxs-lookup"><span data-stu-id="cb86a-122">Basic</span></span>
- <span data-ttu-id="cb86a-123">Ingyenes</span><span class="sxs-lookup"><span data-stu-id="cb86a-123">Free</span></span>

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

### <span data-ttu-id="cb86a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb86a-124">-ResourceGroupName</span></span>
<span data-ttu-id="cb86a-125">Annak az erőforrás-csoportnak a nevét adja meg, amely a parancsmag által módosított automatizálási fiókot tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="cb86a-125">Specifies the name of a resource group that contains the Automation account that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="cb86a-126">-Címkék</span><span class="sxs-lookup"><span data-stu-id="cb86a-126">-Tags</span></span>
<span data-ttu-id="cb86a-127">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="cb86a-127">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="cb86a-128">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="cb86a-128">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="cb86a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb86a-129">CommonParameters</span></span>
<span data-ttu-id="cb86a-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cb86a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb86a-131">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb86a-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb86a-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cb86a-132">INPUTS</span></span>

### <span data-ttu-id="cb86a-133">System. String</span><span class="sxs-lookup"><span data-stu-id="cb86a-133">System.String</span></span>

### <span data-ttu-id="cb86a-134">System. Collections. IDictionary</span><span class="sxs-lookup"><span data-stu-id="cb86a-134">System.Collections.IDictionary</span></span>

## <span data-ttu-id="cb86a-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cb86a-135">OUTPUTS</span></span>

### <span data-ttu-id="cb86a-136">Microsoft. Azure. Command. Automation. Model. AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="cb86a-136">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="cb86a-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cb86a-137">NOTES</span></span>

## <span data-ttu-id="cb86a-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cb86a-138">RELATED LINKS</span></span>

[<span data-ttu-id="cb86a-139">Get-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="cb86a-139">Get-AzAutomationAccount</span></span>](./Get-AzAutomationAccount.md)

[<span data-ttu-id="cb86a-140">Új – AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="cb86a-140">New-AzAutomationAccount</span></span>](./New-AzAutomationAccount.md)

[<span data-ttu-id="cb86a-141">Remove-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="cb86a-141">Remove-AzAutomationAccount</span></span>](./Remove-AzAutomationAccount.md)
