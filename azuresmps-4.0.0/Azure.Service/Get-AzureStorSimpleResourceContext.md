---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 7CB42968-8F6F-4D84-9AE2-1000F280BF3C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 586abbd5f203ce00f6faa7975d9e2adbd0c7940e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016549"
---
# <span data-ttu-id="5d250-101">Get-AzureStorSimpleResourceContext</span><span class="sxs-lookup"><span data-stu-id="5d250-101">Get-AzureStorSimpleResourceContext</span></span>

## <span data-ttu-id="5d250-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5d250-102">SYNOPSIS</span></span>
<span data-ttu-id="5d250-103">Az aktuális erőforrás környezetének beolvasása</span><span class="sxs-lookup"><span data-stu-id="5d250-103">Gets the current resource context.</span></span>

## <span data-ttu-id="5d250-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5d250-104">SYNTAX</span></span>

```
Get-AzureStorSimpleResourceContext [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="5d250-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5d250-105">DESCRIPTION</span></span>
<span data-ttu-id="5d250-106">A **Get-AzureStorSimpleResourceContext** parancsmag a jelenlegi erőforrás-környezetet kapja.</span><span class="sxs-lookup"><span data-stu-id="5d250-106">The **Get-AzureStorSimpleResourceContext** cmdlet gets the current resource context.</span></span>

## <span data-ttu-id="5d250-107">Példák</span><span class="sxs-lookup"><span data-stu-id="5d250-107">EXAMPLES</span></span>

### <span data-ttu-id="5d250-108">Példa 1: az aktuális környezet beszerzése</span><span class="sxs-lookup"><span data-stu-id="5d250-108">Example 1: Get the current context</span></span>
```
PS C:\>Select-AzureStorSimpleResource -ResourceName "Contoso63-Tsqa" 
PS C:\> Get-AzureStorSimpleResourceContext
ResourceId           ResourceName
----------           ------------
1909806764156522689  Contoso63-Tsqa
```

<span data-ttu-id="5d250-109">Az első parancs a **Select-AzureStorSimpleResource** parancsmaggal állítja be az aktuális környezetet a Contoso63-Tsqa nevű erőforráshoz.</span><span class="sxs-lookup"><span data-stu-id="5d250-109">The first command sets the current context to be the resource named Contoso63-Tsqa by using the **Select-AzureStorSimpleResource** cmdlet.</span></span>

<span data-ttu-id="5d250-110">A második parancs a jelenlegi erőforrás-környezetet kapja.</span><span class="sxs-lookup"><span data-stu-id="5d250-110">The second command gets the current resource context.</span></span>

### <span data-ttu-id="5d250-111">2. példa: az aktuális környezet beszerzésének kísérlete</span><span class="sxs-lookup"><span data-stu-id="5d250-111">Example 2: Attempt to get the current context</span></span>
```
PS C:\>Get-AzureStorSimpleResourceContext
Get-AzureStorSimpleResourceContext : Resource Context is not set for your subscription. Please use
Select-AzureStorSimpleResource -ResourceName <<name>> to set
```

<span data-ttu-id="5d250-112">Ez a parancs a jelenlegi környezetet kapja.</span><span class="sxs-lookup"><span data-stu-id="5d250-112">This command gets the current context.</span></span>
<span data-ttu-id="5d250-113">Ebben a példában nincs beállítva környezet.</span><span class="sxs-lookup"><span data-stu-id="5d250-113">In this example, no context has been set.</span></span>
<span data-ttu-id="5d250-114">A parancs olyan üzenetet ad eredményül, amely ismerteti a problémát.</span><span class="sxs-lookup"><span data-stu-id="5d250-114">The command returns a message that explains the problem.</span></span>

## <span data-ttu-id="5d250-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5d250-115">PARAMETERS</span></span>

### <span data-ttu-id="5d250-116">-Profil</span><span class="sxs-lookup"><span data-stu-id="5d250-116">-Profile</span></span>
<span data-ttu-id="5d250-117">Egy Azure-profilt ad meg.</span><span class="sxs-lookup"><span data-stu-id="5d250-117">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="5d250-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d250-118">CommonParameters</span></span>
<span data-ttu-id="5d250-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5d250-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d250-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d250-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d250-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5d250-121">INPUTS</span></span>

### <span data-ttu-id="5d250-122">Nincs</span><span class="sxs-lookup"><span data-stu-id="5d250-122">None</span></span>

## <span data-ttu-id="5d250-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5d250-123">OUTPUTS</span></span>

### <span data-ttu-id="5d250-124">StorSimpleResourceContext</span><span class="sxs-lookup"><span data-stu-id="5d250-124">StorSimpleResourceContext</span></span>
<span data-ttu-id="5d250-125">Ez a parancsmag egy **ResourceContext** objektumot ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="5d250-125">This cmdlet returns a **ResourceContext** object.</span></span>

## <span data-ttu-id="5d250-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5d250-126">NOTES</span></span>

## <span data-ttu-id="5d250-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5d250-127">RELATED LINKS</span></span>

[<span data-ttu-id="5d250-128">Get-AzureStorSimpleResource</span><span class="sxs-lookup"><span data-stu-id="5d250-128">Get-AzureStorSimpleResource</span></span>](./Get-AzureStorSimpleResource.md)

[<span data-ttu-id="5d250-129">Select-AzureStorSimpleResource</span><span class="sxs-lookup"><span data-stu-id="5d250-129">Select-AzureStorSimpleResource</span></span>](./Select-AzureStorSimpleResource.md)


