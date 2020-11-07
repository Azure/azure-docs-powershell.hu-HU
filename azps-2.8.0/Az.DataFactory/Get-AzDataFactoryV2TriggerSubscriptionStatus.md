---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2triggersubscriptionstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2TriggerSubscriptionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2TriggerSubscriptionStatus.md
ms.openlocfilehash: fedb3db8ae8d7cd64ab4309da65f9dea998826e4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667043"
---
# <span data-ttu-id="21f7f-101">Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="21f7f-101">Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>

## <span data-ttu-id="21f7f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="21f7f-102">SYNOPSIS</span></span>
<span data-ttu-id="21f7f-103">Az esemény eseményindítójának állapotát a megadott külső szolgáltatási eseményekre vonatkozóan szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="21f7f-103">Get the status of the subscription for the event trigger to the specified external service events.</span></span>

## <span data-ttu-id="21f7f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="21f7f-104">SYNTAX</span></span>

### <span data-ttu-id="21f7f-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="21f7f-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2TriggerSubscriptionStatus [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="21f7f-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="21f7f-106">ByInputObject</span></span>
```
Get-AzDataFactoryV2TriggerSubscriptionStatus [-InputObject] <PSTrigger>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="21f7f-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="21f7f-107">ByResourceId</span></span>
```
Get-AzDataFactoryV2TriggerSubscriptionStatus [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="21f7f-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="21f7f-108">DESCRIPTION</span></span>
<span data-ttu-id="21f7f-109">Ez a parancs beolvassa az eseményhez tartozó előfizetés állapotát a megadott külső szolgáltatási eseményekhez.</span><span class="sxs-lookup"><span data-stu-id="21f7f-109">This command gets the status of the subscription for the event trigger to the specified external service events.</span></span> <span data-ttu-id="21f7f-110">Az indító nem indítható el, amíg a visszaadott állapot "engedélyezve" nem van.</span><span class="sxs-lookup"><span data-stu-id="21f7f-110">The trigger can't be started until the returned status is "Enabled".</span></span>

## <span data-ttu-id="21f7f-111">Példák</span><span class="sxs-lookup"><span data-stu-id="21f7f-111">EXAMPLES</span></span>

### <span data-ttu-id="21f7f-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="21f7f-112">Example 1</span></span>
```
PS C:\> Get-AzDataFactoryV2TriggerSubscriptionStatus -ResourceGroupName ADF -DataFactoryName WikiADF -Name Trigger1

TriggerName Status
----------- ------
Trigger1    Enabled
```

<span data-ttu-id="21f7f-113">Ez a parancs a BlobEnetTrigger1 Subscribtion állapotát jeleníti meg a külső szolgáltatási eseményekhez.</span><span class="sxs-lookup"><span data-stu-id="21f7f-113">This command will get the status of the subscribtion for BlobEnetTrigger1 trigger to the external service events.</span></span>

## <span data-ttu-id="21f7f-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="21f7f-114">PARAMETERS</span></span>

### <span data-ttu-id="21f7f-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="21f7f-115">-DataFactoryName</span></span>
<span data-ttu-id="21f7f-116">Az adatgyári név.</span><span class="sxs-lookup"><span data-stu-id="21f7f-116">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21f7f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21f7f-117">-DefaultProfile</span></span>
<span data-ttu-id="21f7f-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="21f7f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21f7f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="21f7f-119">-InputObject</span></span>
<span data-ttu-id="21f7f-120">Az indító objektum.</span><span class="sxs-lookup"><span data-stu-id="21f7f-120">The trigger object.</span></span>

```yaml
Type: PSTrigger
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="21f7f-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="21f7f-121">-Name</span></span>
<span data-ttu-id="21f7f-122">Az indító neve.</span><span class="sxs-lookup"><span data-stu-id="21f7f-122">The trigger name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21f7f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21f7f-123">-ResourceGroupName</span></span>
<span data-ttu-id="21f7f-124">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="21f7f-124">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21f7f-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="21f7f-125">-ResourceId</span></span>
<span data-ttu-id="21f7f-126">Az Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="21f7f-126">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21f7f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21f7f-127">CommonParameters</span></span>
<span data-ttu-id="21f7f-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="21f7f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21f7f-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21f7f-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21f7f-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="21f7f-130">INPUTS</span></span>

### <span data-ttu-id="21f7f-131">System. String</span><span class="sxs-lookup"><span data-stu-id="21f7f-131">System.String</span></span>
<span data-ttu-id="21f7f-132">Microsoft. Azure. Command. DataFactoryV2. models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="21f7f-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="21f7f-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="21f7f-133">OUTPUTS</span></span>

### <span data-ttu-id="21f7f-134">Microsoft. Azure. Command. DataFactoryV2. models. PSTriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="21f7f-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerSubscriptionStatus</span></span>

## <span data-ttu-id="21f7f-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="21f7f-135">NOTES</span></span>

## <span data-ttu-id="21f7f-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="21f7f-136">RELATED LINKS</span></span>

