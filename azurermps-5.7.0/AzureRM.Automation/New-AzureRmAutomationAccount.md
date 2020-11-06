---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 2D5B16F0-0662-4D9F-A13F-808CE5EEBBA3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/new-azurermautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationAccount.md
ms.openlocfilehash: c82a68e7859945b1fdb91f6d44a1ebbcef6d2cff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493286"
---
# <span data-ttu-id="76037-101">New-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="76037-101">New-AzureRmAutomationAccount</span></span>

## <span data-ttu-id="76037-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="76037-102">SYNOPSIS</span></span>
<span data-ttu-id="76037-103">Automatizálási fiókot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="76037-103">Creates an Automation account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="76037-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="76037-104">SYNTAX</span></span>

```
New-AzureRmAutomationAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Plan <String>] [-Tags <IDictionary>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="76037-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="76037-105">DESCRIPTION</span></span>
<span data-ttu-id="76037-106">A **New-AzureRmAutomationAccount** parancsmag Azure automatizálási fiókot hoz létre egy erőforráscsoportben.</span><span class="sxs-lookup"><span data-stu-id="76037-106">The **New-AzureRmAutomationAccount** cmdlet creates an Azure Automation account in a resource group.</span></span>

<span data-ttu-id="76037-107">Az automatizálási fiók a többi automatizálási fiók erőforrásaitól elkülönített automatizálási erőforrások tárolója.</span><span class="sxs-lookup"><span data-stu-id="76037-107">An Automation account is a container for Automation resources that is isolated from the resources of other Automation accounts.</span></span> <span data-ttu-id="76037-108">Az automatizálási erőforrások közé tartozik a runbooks, a kívánt állapot-konfiguráció (DSC), a feladatok és az eszközök.</span><span class="sxs-lookup"><span data-stu-id="76037-108">Automation resources include runbooks, Desired State Configuration (DSC) configurations, jobs, and assets.</span></span>

## <span data-ttu-id="76037-109">Példák</span><span class="sxs-lookup"><span data-stu-id="76037-109">EXAMPLES</span></span>

### <span data-ttu-id="76037-110">Példa 1: automatizálási fiók létrehozása</span><span class="sxs-lookup"><span data-stu-id="76037-110">Example 1: Create an automation account</span></span>
```
PS C:\> New-AzureRmAutomationAccount -Name "ContosoAutomationAccount" -Location "East US" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="76037-111">Ez a parancs létrehoz egy ContosoAutomationAccount nevű új automatizálási fiókot a kelet-amerikai régióban.</span><span class="sxs-lookup"><span data-stu-id="76037-111">This command creates a new automation account named ContosoAutomationAccount in the East US region.</span></span>

## <span data-ttu-id="76037-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="76037-112">PARAMETERS</span></span>

### <span data-ttu-id="76037-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76037-113">-DefaultProfile</span></span>
<span data-ttu-id="76037-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="76037-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76037-115">-Hely</span><span class="sxs-lookup"><span data-stu-id="76037-115">-Location</span></span>
<span data-ttu-id="76037-116">Azt a helyet adja meg, ahol ez a parancsmag létrehoz egy automatizálási fiókot.</span><span class="sxs-lookup"><span data-stu-id="76037-116">Specifies the location in which this cmdlet creates the Automation account.</span></span>
<span data-ttu-id="76037-117">Ha érvényes helyeket szeretne beolvasni, használja az Get-AzureRMLocation parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="76037-117">To obtain valid locations, use the Get-AzureRMLocation cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76037-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="76037-118">-Name</span></span>
<span data-ttu-id="76037-119">Az automatizálási fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="76037-119">Specifies a name for the Automation account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AutomationAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76037-120">-Terv</span><span class="sxs-lookup"><span data-stu-id="76037-120">-Plan</span></span>
<span data-ttu-id="76037-121">Az automatizálási fiók tervét adja meg.</span><span class="sxs-lookup"><span data-stu-id="76037-121">Specifies the plan for the Automation account.</span></span>
<span data-ttu-id="76037-122">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="76037-122">Valid values are:</span></span>

- <span data-ttu-id="76037-123">Egyszerű</span><span class="sxs-lookup"><span data-stu-id="76037-123">Basic</span></span>
- <span data-ttu-id="76037-124">Ingyenes</span><span class="sxs-lookup"><span data-stu-id="76037-124">Free</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Free, Basic

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76037-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76037-125">-ResourceGroupName</span></span>
<span data-ttu-id="76037-126">Annak az erőforráscsoportnek a nevét adja meg, amelyre a parancsmag automatizálási fiókot ad.</span><span class="sxs-lookup"><span data-stu-id="76037-126">Specifies the name of a resource group to which this cmdlet adds an Automation account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76037-127">-Címkék</span><span class="sxs-lookup"><span data-stu-id="76037-127">-Tags</span></span>
<span data-ttu-id="76037-128">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="76037-128">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="76037-129">Példa:</span><span class="sxs-lookup"><span data-stu-id="76037-129">For example:</span></span>

<span data-ttu-id="76037-130">@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="76037-130">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76037-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76037-131">CommonParameters</span></span>
<span data-ttu-id="76037-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="76037-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76037-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76037-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76037-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="76037-134">INPUTS</span></span>

### <span data-ttu-id="76037-135">Nincs</span><span class="sxs-lookup"><span data-stu-id="76037-135">None</span></span>
<span data-ttu-id="76037-136">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="76037-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="76037-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="76037-137">OUTPUTS</span></span>

### <span data-ttu-id="76037-138">Microsoft. Azure. Command. Automation. Model. AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="76037-138">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="76037-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="76037-139">NOTES</span></span>

## <span data-ttu-id="76037-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="76037-140">RELATED LINKS</span></span>

[<span data-ttu-id="76037-141">Get-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="76037-141">Get-AzureRmAutomationAccount</span></span>](./Get-AzureRmAutomationAccount.md)

[<span data-ttu-id="76037-142">Remove-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="76037-142">Remove-AzureRmAutomationAccount</span></span>](./Remove-AzureRmAutomationAccount.md)

[<span data-ttu-id="76037-143">Set-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="76037-143">Set-AzureRmAutomationAccount</span></span>](./Set-AzureRmAutomationAccount.md)
