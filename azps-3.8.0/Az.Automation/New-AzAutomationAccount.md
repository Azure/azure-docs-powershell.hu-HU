---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 2D5B16F0-0662-4D9F-A13F-808CE5EEBBA3
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationAccount.md
ms.openlocfilehash: 350e1591081e1d171921a432a1b990066614c750
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014978"
---
# <span data-ttu-id="2d8df-101">New-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="2d8df-101">New-AzAutomationAccount</span></span>

## <span data-ttu-id="2d8df-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2d8df-102">SYNOPSIS</span></span>
<span data-ttu-id="2d8df-103">Automatizálási fiókot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="2d8df-103">Creates an Automation account.</span></span>

## <span data-ttu-id="2d8df-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2d8df-104">SYNTAX</span></span>

```
New-AzAutomationAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Plan <String>]
 [-Tags <IDictionary>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2d8df-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2d8df-105">DESCRIPTION</span></span>
<span data-ttu-id="2d8df-106">A **New-AzAutomationAccount** parancsmag Azure automatizálási fiókot hoz létre egy erőforráscsoportben.</span><span class="sxs-lookup"><span data-stu-id="2d8df-106">The **New-AzAutomationAccount** cmdlet creates an Azure Automation account in a resource group.</span></span>
<span data-ttu-id="2d8df-107">Az automatizálási fiók a többi automatizálási fiók erőforrásaitól elkülönített automatizálási erőforrások tárolója.</span><span class="sxs-lookup"><span data-stu-id="2d8df-107">An Automation account is a container for Automation resources that is isolated from the resources of other Automation accounts.</span></span> <span data-ttu-id="2d8df-108">Az automatizálási erőforrások közé tartozik a runbooks, a kívánt állapot-konfiguráció (DSC), a feladatok és az eszközök.</span><span class="sxs-lookup"><span data-stu-id="2d8df-108">Automation resources include runbooks, Desired State Configuration (DSC) configurations, jobs, and assets.</span></span>

## <span data-ttu-id="2d8df-109">Példák</span><span class="sxs-lookup"><span data-stu-id="2d8df-109">EXAMPLES</span></span>

### <span data-ttu-id="2d8df-110">Példa 1: automatizálási fiók létrehozása</span><span class="sxs-lookup"><span data-stu-id="2d8df-110">Example 1: Create an automation account</span></span>
```
PS C:\> New-AzAutomationAccount -Name "ContosoAutomationAccount" -Location "East US" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="2d8df-111">Ez a parancs létrehoz egy ContosoAutomationAccount nevű új automatizálási fiókot a kelet-amerikai régióban.</span><span class="sxs-lookup"><span data-stu-id="2d8df-111">This command creates a new automation account named ContosoAutomationAccount in the East US region.</span></span>

## <span data-ttu-id="2d8df-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2d8df-112">PARAMETERS</span></span>

### <span data-ttu-id="2d8df-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d8df-113">-DefaultProfile</span></span>
<span data-ttu-id="2d8df-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="2d8df-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2d8df-115">-Hely</span><span class="sxs-lookup"><span data-stu-id="2d8df-115">-Location</span></span>
<span data-ttu-id="2d8df-116">Azt a helyet adja meg, ahol ez a parancsmag létrehoz egy automatizálási fiókot.</span><span class="sxs-lookup"><span data-stu-id="2d8df-116">Specifies the location in which this cmdlet creates the Automation account.</span></span>
<span data-ttu-id="2d8df-117">Ha érvényes helyeket szeretne beolvasni, használja az Get-AzLocation parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="2d8df-117">To obtain valid locations, use the Get-AzLocation cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d8df-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2d8df-118">-Name</span></span>
<span data-ttu-id="2d8df-119">Az automatizálási fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2d8df-119">Specifies a name for the Automation account.</span></span>

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

### <span data-ttu-id="2d8df-120">-Terv</span><span class="sxs-lookup"><span data-stu-id="2d8df-120">-Plan</span></span>
<span data-ttu-id="2d8df-121">Az automatizálási fiók tervét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2d8df-121">Specifies the plan for the Automation account.</span></span>
<span data-ttu-id="2d8df-122">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="2d8df-122">Valid values are:</span></span>
- <span data-ttu-id="2d8df-123">Egyszerű</span><span class="sxs-lookup"><span data-stu-id="2d8df-123">Basic</span></span>
- <span data-ttu-id="2d8df-124">Ingyenes</span><span class="sxs-lookup"><span data-stu-id="2d8df-124">Free</span></span>

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

### <span data-ttu-id="2d8df-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d8df-125">-ResourceGroupName</span></span>
<span data-ttu-id="2d8df-126">Annak az erőforráscsoportnek a nevét adja meg, amelyre a parancsmag automatizálási fiókot ad.</span><span class="sxs-lookup"><span data-stu-id="2d8df-126">Specifies the name of a resource group to which this cmdlet adds an Automation account.</span></span>

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

### <span data-ttu-id="2d8df-127">-Címkék</span><span class="sxs-lookup"><span data-stu-id="2d8df-127">-Tags</span></span>
<span data-ttu-id="2d8df-128">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="2d8df-128">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="2d8df-129">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="2d8df-129">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="2d8df-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d8df-130">CommonParameters</span></span>
<span data-ttu-id="2d8df-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2d8df-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d8df-132">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d8df-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d8df-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2d8df-133">INPUTS</span></span>

### <span data-ttu-id="2d8df-134">System. String</span><span class="sxs-lookup"><span data-stu-id="2d8df-134">System.String</span></span>

### <span data-ttu-id="2d8df-135">System. Collections. IDictionary</span><span class="sxs-lookup"><span data-stu-id="2d8df-135">System.Collections.IDictionary</span></span>

## <span data-ttu-id="2d8df-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2d8df-136">OUTPUTS</span></span>

### <span data-ttu-id="2d8df-137">Microsoft. Azure. Command. Automation. Model. AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="2d8df-137">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="2d8df-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2d8df-138">NOTES</span></span>

## <span data-ttu-id="2d8df-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2d8df-139">RELATED LINKS</span></span>

[<span data-ttu-id="2d8df-140">Get-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="2d8df-140">Get-AzAutomationAccount</span></span>](./Get-AzAutomationAccount.md)

[<span data-ttu-id="2d8df-141">Remove-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="2d8df-141">Remove-AzAutomationAccount</span></span>](./Remove-AzAutomationAccount.md)

[<span data-ttu-id="2d8df-142">Set-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="2d8df-142">Set-AzAutomationAccount</span></span>](./Set-AzAutomationAccount.md)
