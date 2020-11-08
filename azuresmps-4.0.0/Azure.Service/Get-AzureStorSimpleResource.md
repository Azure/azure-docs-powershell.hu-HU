---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 482E8CD6-C38F-4BD5-8214-016D0D8C7FD0
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6381b8e0fac5ebf047122f131af6087d5bb5a9fb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015554"
---
# <span data-ttu-id="8b680-101">Get-AzureStorSimpleResource</span><span class="sxs-lookup"><span data-stu-id="8b680-101">Get-AzureStorSimpleResource</span></span>

## <span data-ttu-id="8b680-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8b680-102">SYNOPSIS</span></span>
<span data-ttu-id="8b680-103">A létrehozott összes erőforrást megkapja.</span><span class="sxs-lookup"><span data-stu-id="8b680-103">Gets all resources that you created.</span></span>

## <span data-ttu-id="8b680-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8b680-104">SYNTAX</span></span>

```
Get-AzureStorSimpleResource [-ResourceName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="8b680-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8b680-105">DESCRIPTION</span></span>
<span data-ttu-id="8b680-106">A **Get-AzureStorSimpleResource** parancsmag az Azure Portal használatával létrehozott összes erőforrást megkapja.</span><span class="sxs-lookup"><span data-stu-id="8b680-106">The **Get-AzureStorSimpleResource** cmdlet gets all resources that you created by using Azure Portal.</span></span>
<span data-ttu-id="8b680-107">A parancsmag az erőforrásokhoz való csatlakozáshoz használható részleteket tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="8b680-107">The cmdlet gets details you can use to connect to the resources.</span></span>

## <span data-ttu-id="8b680-108">Példák</span><span class="sxs-lookup"><span data-stu-id="8b680-108">EXAMPLES</span></span>

### <span data-ttu-id="8b680-109">Példa 1: az összes erőforrás beolvasása</span><span class="sxs-lookup"><span data-stu-id="8b680-109">Example 1: Get all resources</span></span>
```
PS C:\>Get-AzureStorSimpleResource
VERBOSE: ClientRequestId: 5cd61b91-ef40-43b4-986d-156e06d2ed65_PS

ResourceName                                      ResourceId           ResourceState
------------                                      ----------           -------------
Contoso63-Tsqa                                    8838459798595306468  Started
Contoso68-Tsqa                                    2859070203638134681  Started
Contoso73-Tsqa                                    7871392677286863733  Started
Contoso87-Tsqa                                    1909806764156522689  Started
VERBOSE: Found 4 StorSimple resources.
```

<span data-ttu-id="8b680-110">Ez a parancs minden létrehozott erőforrást megkapja.</span><span class="sxs-lookup"><span data-stu-id="8b680-110">This command gets all the resources you created.</span></span>
<span data-ttu-id="8b680-111">Ebben a példában három erőforrás áll rendelkezésre.</span><span class="sxs-lookup"><span data-stu-id="8b680-111">In this example, there are three resources.</span></span>

### <span data-ttu-id="8b680-112">2. példa: erőforrás beszerzése a neve alapján</span><span class="sxs-lookup"><span data-stu-id="8b680-112">Example 2: Get a resource by using its name</span></span>
```
PS C:\>Get-AzureStorSimpleResource -ResourceName "Contoso63-Tsqa"
VERBOSE: ClientRequestId: efc3c85c-12aa-4345-b6eb-ccc532de4825_PS

ResourceName                                      ResourceId           ResourceState
------------                                      ----------           -------------
Contoso63-Tsqa                                    1909806764156522689  Started
VERBOSE: Found 1 StorSimple resource.
```

<span data-ttu-id="8b680-113">Ez a parancs a Contoso63-Tsqa nevű erőforrást kapja.</span><span class="sxs-lookup"><span data-stu-id="8b680-113">This command gets the resource named Contoso63-Tsqa.</span></span>

### <span data-ttu-id="8b680-114">3. példa: nem létező erőforrás beszerzésének kísérlete</span><span class="sxs-lookup"><span data-stu-id="8b680-114">Example 3: Attempt to get a nonexistent resource</span></span>
```
PS C:\>Get-AzureStorSimpleResource -ResourceName "Contoso64-Tsqa"
VERBOSE: ClientRequestId: 5d08d40b-f9d7-4d43-956f-13f01e89625b_PS
VERBOSE: Invalid input : Could not find a resource named Contoso64-Tsqa in your subscription.
```

<span data-ttu-id="8b680-115">Ez a parancs megkísérli a Contoso64-Tsqa nevű erőforrás beszerzését.</span><span class="sxs-lookup"><span data-stu-id="8b680-115">This command attempts to get the resource named Contoso64-Tsqa.</span></span>
<span data-ttu-id="8b680-116">Nincs ilyen nevű erőforrás.</span><span class="sxs-lookup"><span data-stu-id="8b680-116">There is no resource that has this name.</span></span>
<span data-ttu-id="8b680-117">Ez a példa nem ad vissza erőforrást.</span><span class="sxs-lookup"><span data-stu-id="8b680-117">This example does not return any resource.</span></span>

## <span data-ttu-id="8b680-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8b680-118">PARAMETERS</span></span>

### <span data-ttu-id="8b680-119">-Profil</span><span class="sxs-lookup"><span data-stu-id="8b680-119">-Profile</span></span>
<span data-ttu-id="8b680-120">Egy Azure-profilt ad meg.</span><span class="sxs-lookup"><span data-stu-id="8b680-120">Specifies an Azure profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b680-121">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="8b680-121">-ResourceName</span></span>
<span data-ttu-id="8b680-122">Itt adhatja meg annak az erőforrásnak a nevét, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="8b680-122">Specifies the name of the resource that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b680-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b680-123">CommonParameters</span></span>
<span data-ttu-id="8b680-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8b680-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b680-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b680-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b680-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8b680-126">INPUTS</span></span>

### <span data-ttu-id="8b680-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="8b680-127">None</span></span>

## <span data-ttu-id="8b680-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8b680-128">OUTPUTS</span></span>

### <span data-ttu-id="8b680-129">IEnumerable \<ResourceCredentials\> , ResourceCredentials</span><span class="sxs-lookup"><span data-stu-id="8b680-129">IEnumerable\<ResourceCredentials\>, ResourceCredentials</span></span>
<span data-ttu-id="8b680-130">Ez a parancsmag a következő tulajdonságokat tartalmazó **ResourceCredentials** -objektumokat ad eredményül:</span><span class="sxs-lookup"><span data-stu-id="8b680-130">This cmdlet returns **ResourceCredentials** objects that contain the following properties:</span></span> 

- <span data-ttu-id="8b680-131">**ResourceName**</span><span class="sxs-lookup"><span data-stu-id="8b680-131">**ResourceName**</span></span>
- <span data-ttu-id="8b680-132">**ResouceId**</span><span class="sxs-lookup"><span data-stu-id="8b680-132">**ResouceId**</span></span>
- <span data-ttu-id="8b680-133">**ResourceState**</span><span class="sxs-lookup"><span data-stu-id="8b680-133">**ResourceState**</span></span>

## <span data-ttu-id="8b680-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8b680-134">NOTES</span></span>

## <span data-ttu-id="8b680-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8b680-135">RELATED LINKS</span></span>

[<span data-ttu-id="8b680-136">Get-AzureStorSimpleResourceContext</span><span class="sxs-lookup"><span data-stu-id="8b680-136">Get-AzureStorSimpleResourceContext</span></span>](./Get-AzureStorSimpleResourceContext.md)

[<span data-ttu-id="8b680-137">Select-AzureStorSimpleResource</span><span class="sxs-lookup"><span data-stu-id="8b680-137">Select-AzureStorSimpleResource</span></span>](./Select-AzureStorSimpleResource.md)


