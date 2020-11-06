---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B1897EFC-0184-4A8B-B8E4-203CC8E3B179
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRmAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRmAutomationAccount.md
ms.openlocfilehash: 8ad63c37c366c0f9c7693585f3a3c2fd57de4fdd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493876"
---
# <span data-ttu-id="59826-101">Set-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="59826-101">Set-AzureRmAutomationAccount</span></span>

## <span data-ttu-id="59826-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="59826-102">SYNOPSIS</span></span>
<span data-ttu-id="59826-103">Automatizálási fiók módosítása</span><span class="sxs-lookup"><span data-stu-id="59826-103">Modifies an Automation account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="59826-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="59826-104">SYNTAX</span></span>

```
Set-AzureRmAutomationAccount [-ResourceGroupName] <String> [-Name] <String> [-Plan <String>]
 [-Tags <IDictionary>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="59826-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="59826-105">DESCRIPTION</span></span>
<span data-ttu-id="59826-106">A **set-AzureRmAutomationAccount** parancsmag az Azure automatizálási fiókját módosítja.</span><span class="sxs-lookup"><span data-stu-id="59826-106">The **Set-AzureRmAutomationAccount** cmdlet modifies an Azure Automation account.</span></span>

<span data-ttu-id="59826-107">Az automatizálási fiókokról további információt az New-AzureRmAutomationAccount parancsmag című témakörben találhat.</span><span class="sxs-lookup"><span data-stu-id="59826-107">For more information about Automation accounts, see the New-AzureRmAutomationAccount cmdlet.</span></span>

## <span data-ttu-id="59826-108">Példák</span><span class="sxs-lookup"><span data-stu-id="59826-108">EXAMPLES</span></span>

### <span data-ttu-id="59826-109">Példa 1: automatizálási fiók címkékének beállítása</span><span class="sxs-lookup"><span data-stu-id="59826-109">Example 1: Set the tags for an Automation account</span></span>
```
PS C:\>$Tags = @{"tag01"="value01";"tag02"="value02"}
PS C:\> Set-AzureRmAutomationAccount -Name "AutomationAccount01" -ResourceGroupName "ResourceGroup01" -Tags $Tags
```

<span data-ttu-id="59826-110">Az első parancs két kulcs/érték párokat rendel a $Tags változóhoz.</span><span class="sxs-lookup"><span data-stu-id="59826-110">The first command assigns two key/value pairs to the $Tags variable.</span></span>

<span data-ttu-id="59826-111">A második parancs a AutomationAccount01 nevű automatizálási fiókhoz $Tags címkéket állít be.</span><span class="sxs-lookup"><span data-stu-id="59826-111">The second command sets tags in $Tags for the Automation account named AutomationAccount01.</span></span>

### <span data-ttu-id="59826-112">2. példa: az automatizálási fiók tervének módosítása</span><span class="sxs-lookup"><span data-stu-id="59826-112">Example 2: Change the plan for an Automation account</span></span>
```
PS C:\>Set-AzureRmAutomationAccount -Name "AutomationAccount01" -ResourceGroupName "ResourceGroup01" -Plan Basic
```

<span data-ttu-id="59826-113">Ez a parancs a AutomationAccount01 nevű automatizálási fiók esetében módosítja az alaptervet.</span><span class="sxs-lookup"><span data-stu-id="59826-113">This command changes the plan to Basic for the Automation account named AutomationAccount01.</span></span>

## <span data-ttu-id="59826-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="59826-114">PARAMETERS</span></span>

### <span data-ttu-id="59826-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="59826-115">-Name</span></span>
<span data-ttu-id="59826-116">A parancsmag által módosított automatizálási fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="59826-116">Specifies the name of the Automation account that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="59826-117">-Terv</span><span class="sxs-lookup"><span data-stu-id="59826-117">-Plan</span></span>
<span data-ttu-id="59826-118">Az automatizálási fiók tervét adja meg.</span><span class="sxs-lookup"><span data-stu-id="59826-118">Specifies the plan for the Automation account.</span></span>
<span data-ttu-id="59826-119">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="59826-119">Valid values are:</span></span>

- <span data-ttu-id="59826-120">Egyszerű</span><span class="sxs-lookup"><span data-stu-id="59826-120">Basic</span></span>
- <span data-ttu-id="59826-121">Ingyenes</span><span class="sxs-lookup"><span data-stu-id="59826-121">Free</span></span>

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

### <span data-ttu-id="59826-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59826-122">-ResourceGroupName</span></span>
<span data-ttu-id="59826-123">Annak az erőforrás-csoportnak a nevét adja meg, amely a parancsmag által módosított automatizálási fiókot tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="59826-123">Specifies the name of a resource group that contains the Automation account that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="59826-124">-Címkék</span><span class="sxs-lookup"><span data-stu-id="59826-124">-Tags</span></span>
<span data-ttu-id="59826-125">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="59826-125">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="59826-126">Példa:</span><span class="sxs-lookup"><span data-stu-id="59826-126">For example:</span></span>

<span data-ttu-id="59826-127">@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="59826-127">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="59826-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59826-128">-DefaultProfile</span></span>
<span data-ttu-id="59826-129">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="59826-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59826-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59826-130">CommonParameters</span></span>
<span data-ttu-id="59826-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="59826-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59826-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59826-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59826-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="59826-133">INPUTS</span></span>

## <span data-ttu-id="59826-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="59826-134">OUTPUTS</span></span>

### <span data-ttu-id="59826-135">Microsoft. Azure. Command. Automation. Model. AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="59826-135">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="59826-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="59826-136">NOTES</span></span>

## <span data-ttu-id="59826-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="59826-137">RELATED LINKS</span></span>

[<span data-ttu-id="59826-138">Get-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="59826-138">Get-AzureRmAutomationAccount</span></span>](./Get-AzureRmAutomationAccount.md)

[<span data-ttu-id="59826-139">Új – AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="59826-139">New-AzureRmAutomationAccount</span></span>](./New-AzureRmAutomationAccount.md)

[<span data-ttu-id="59826-140">Remove-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="59826-140">Remove-AzureRmAutomationAccount</span></span>](./Remove-AzureRmAutomationAccount.md)
