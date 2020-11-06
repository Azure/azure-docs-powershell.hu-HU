---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: AFF75E0B-CB88-45ED-9067-7F43E2BA485C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmContainerService.md
ms.openlocfilehash: d2a53d221adf7483899056791aefd00b03aca26e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497740"
---
# <span data-ttu-id="9f7cd-101">Get-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="9f7cd-101">Get-AzureRmContainerService</span></span>

## <span data-ttu-id="9f7cd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9f7cd-102">SYNOPSIS</span></span>
<span data-ttu-id="9f7cd-103">Tároló szolgáltatást kap.</span><span class="sxs-lookup"><span data-stu-id="9f7cd-103">Gets a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9f7cd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9f7cd-104">SYNTAX</span></span>

```
Get-AzureRmContainerService [[-ResourceGroupName] <String>] [[-Name] <String>] [<CommonParameters>]
```

## <span data-ttu-id="9f7cd-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9f7cd-105">DESCRIPTION</span></span>
<span data-ttu-id="9f7cd-106">A **Get-AzureRmContainerService** parancsmag tároló szolgáltatást kap.</span><span class="sxs-lookup"><span data-stu-id="9f7cd-106">The **Get-AzureRmContainerService** cmdlet gets a container service.</span></span>
<span data-ttu-id="9f7cd-107">Megtekintheti a tároló szolgáltatás tulajdonságait, amely tartalmazza az állapotot, a mesteralakzatok számát és az ügynököket, valamint a mesteralakzat és az ügynök teljes tartománynevét is.</span><span class="sxs-lookup"><span data-stu-id="9f7cd-107">You can view the properties of a container service, which include state, number of master and agents, and fully qualified domain name of master and agent.</span></span>

## <span data-ttu-id="9f7cd-108">Példák</span><span class="sxs-lookup"><span data-stu-id="9f7cd-108">EXAMPLES</span></span>

### <span data-ttu-id="9f7cd-109">Példa 1: tároló szolgáltatás beszerzése</span><span class="sxs-lookup"><span data-stu-id="9f7cd-109">Example 1: Get a container service</span></span>
```
PS C:\> Get-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="9f7cd-110">Ez a parancs CSResourceGroup17 nevű tároló szolgáltatást kap.</span><span class="sxs-lookup"><span data-stu-id="9f7cd-110">This command gets a container service named CSResourceGroup17.</span></span>

## <span data-ttu-id="9f7cd-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9f7cd-111">PARAMETERS</span></span>

### <span data-ttu-id="9f7cd-112">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9f7cd-112">-Name</span></span>
<span data-ttu-id="9f7cd-113">Annak a tároló szolgáltatásnak a neve, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="9f7cd-113">Specifies the name of the container service that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f7cd-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f7cd-114">-ResourceGroupName</span></span>
<span data-ttu-id="9f7cd-115">Annak a tároló szolgáltatásnak az erőforrás csoportját adja meg, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="9f7cd-115">Specifies the resource group of the container service that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f7cd-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f7cd-116">CommonParameters</span></span>
<span data-ttu-id="9f7cd-117">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9f7cd-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f7cd-118">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f7cd-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f7cd-119">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9f7cd-119">INPUTS</span></span>

### <span data-ttu-id="9f7cd-120">Nincs</span><span class="sxs-lookup"><span data-stu-id="9f7cd-120">None</span></span>
<span data-ttu-id="9f7cd-121">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="9f7cd-121">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9f7cd-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9f7cd-122">OUTPUTS</span></span>

## <span data-ttu-id="9f7cd-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9f7cd-123">NOTES</span></span>

## <span data-ttu-id="9f7cd-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9f7cd-124">RELATED LINKS</span></span>

[<span data-ttu-id="9f7cd-125">Új – AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="9f7cd-125">New-AzureRmContainerService</span></span>](./New-AzureRmContainerService.md)

[<span data-ttu-id="9f7cd-126">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="9f7cd-126">Remove-AzureRmContainerService</span></span>](./Remove-AzureRmContainerService.md)

[<span data-ttu-id="9f7cd-127">Update-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="9f7cd-127">Update-AzureRmContainerService</span></span>](./Update-AzureRmContainerService.md)


