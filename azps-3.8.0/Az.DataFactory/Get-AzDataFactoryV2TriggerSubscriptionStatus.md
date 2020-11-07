---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2triggersubscriptionstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2TriggerSubscriptionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2TriggerSubscriptionStatus.md
ms.openlocfilehash: 62418f0840e2bbeef016d53c3136f155c4de055f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847265"
---
# <span data-ttu-id="c1eab-101">Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="c1eab-101">Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>

## <span data-ttu-id="c1eab-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c1eab-102">SYNOPSIS</span></span>
<span data-ttu-id="c1eab-103">Az esemény eseményindítójának állapotát a megadott külső szolgáltatási eseményekre vonatkozóan szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="c1eab-103">Get the status of the subscription for the event trigger to the specified external service events.</span></span>

## <span data-ttu-id="c1eab-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c1eab-104">SYNTAX</span></span>

### <span data-ttu-id="c1eab-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c1eab-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2TriggerSubscriptionStatus [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c1eab-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="c1eab-106">ByInputObject</span></span>
```
Get-AzDataFactoryV2TriggerSubscriptionStatus [-InputObject] <PSTrigger>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c1eab-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c1eab-107">ByResourceId</span></span>
```
Get-AzDataFactoryV2TriggerSubscriptionStatus [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c1eab-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="c1eab-108">DESCRIPTION</span></span>
<span data-ttu-id="c1eab-109">Ez a parancs beolvassa az eseményhez tartozó előfizetés állapotát a megadott külső szolgáltatási eseményekhez.</span><span class="sxs-lookup"><span data-stu-id="c1eab-109">This command gets the status of the subscription for the event trigger to the specified external service events.</span></span> <span data-ttu-id="c1eab-110">Az indító nem indítható el, amíg a visszaadott állapot "engedélyezve" nem van.</span><span class="sxs-lookup"><span data-stu-id="c1eab-110">The trigger can't be started until the returned status is "Enabled".</span></span>

## <span data-ttu-id="c1eab-111">Példák</span><span class="sxs-lookup"><span data-stu-id="c1eab-111">EXAMPLES</span></span>

### <span data-ttu-id="c1eab-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="c1eab-112">Example 1</span></span>
```
PS C:\> Get-AzDataFactoryV2TriggerSubscriptionStatus -ResourceGroupName ADF -DataFactoryName WikiADF -Name Trigger1

TriggerName Status
----------- ------
Trigger1    Enabled
```

<span data-ttu-id="c1eab-113">Ez a parancs a BlobEnetTrigger1 Subscribtion állapotát jeleníti meg a külső szolgáltatási eseményekhez.</span><span class="sxs-lookup"><span data-stu-id="c1eab-113">This command will get the status of the subscribtion for BlobEnetTrigger1 trigger to the external service events.</span></span>

## <span data-ttu-id="c1eab-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c1eab-114">PARAMETERS</span></span>

### <span data-ttu-id="c1eab-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="c1eab-115">-DataFactoryName</span></span>
<span data-ttu-id="c1eab-116">Az adatgyári név.</span><span class="sxs-lookup"><span data-stu-id="c1eab-116">The data factory name.</span></span>

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

### <span data-ttu-id="c1eab-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1eab-117">-DefaultProfile</span></span>
<span data-ttu-id="c1eab-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c1eab-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c1eab-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c1eab-119">-InputObject</span></span>
<span data-ttu-id="c1eab-120">Az indító objektum.</span><span class="sxs-lookup"><span data-stu-id="c1eab-120">The trigger object.</span></span>

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

### <span data-ttu-id="c1eab-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c1eab-121">-Name</span></span>
<span data-ttu-id="c1eab-122">Az indító neve.</span><span class="sxs-lookup"><span data-stu-id="c1eab-122">The trigger name.</span></span>

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

### <span data-ttu-id="c1eab-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1eab-123">-ResourceGroupName</span></span>
<span data-ttu-id="c1eab-124">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="c1eab-124">The resource group name.</span></span>

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

### <span data-ttu-id="c1eab-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c1eab-125">-ResourceId</span></span>
<span data-ttu-id="c1eab-126">Az Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="c1eab-126">The Azure resource ID.</span></span>

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

### <span data-ttu-id="c1eab-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1eab-127">CommonParameters</span></span>
<span data-ttu-id="c1eab-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c1eab-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1eab-129">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1eab-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1eab-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c1eab-130">INPUTS</span></span>

### <span data-ttu-id="c1eab-131">System. String</span><span class="sxs-lookup"><span data-stu-id="c1eab-131">System.String</span></span>
<span data-ttu-id="c1eab-132">Microsoft. Azure. Command. DataFactoryV2. models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="c1eab-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="c1eab-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c1eab-133">OUTPUTS</span></span>

### <span data-ttu-id="c1eab-134">Microsoft. Azure. Command. DataFactoryV2. models. PSTriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="c1eab-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerSubscriptionStatus</span></span>

## <span data-ttu-id="c1eab-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c1eab-135">NOTES</span></span>

## <span data-ttu-id="c1eab-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c1eab-136">RELATED LINKS</span></span>

