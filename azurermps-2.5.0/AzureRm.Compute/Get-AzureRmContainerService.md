---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: AFF75E0B-CB88-45ED-9067-7F43E2BA485C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermcontainerservice
schema: 2.0.0
ms.openlocfilehash: 5db21871b84801d57deebf98e27bbe153285631a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850941"
---
# <span data-ttu-id="1e72c-101">Get-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="1e72c-101">Get-AzureRmContainerService</span></span>

## <span data-ttu-id="1e72c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1e72c-102">SYNOPSIS</span></span>
<span data-ttu-id="1e72c-103">Tároló szolgáltatást kap.</span><span class="sxs-lookup"><span data-stu-id="1e72c-103">Gets a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1e72c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1e72c-104">SYNTAX</span></span>

```
Get-AzureRmContainerService [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1e72c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1e72c-105">DESCRIPTION</span></span>
<span data-ttu-id="1e72c-106">A **Get-AzureRmContainerService** parancsmag tároló szolgáltatást kap.</span><span class="sxs-lookup"><span data-stu-id="1e72c-106">The **Get-AzureRmContainerService** cmdlet gets a container service.</span></span>
<span data-ttu-id="1e72c-107">Megtekintheti a tároló szolgáltatás tulajdonságait, amely tartalmazza az állapotot, a mesteralakzatok számát és az ügynököket, valamint a mesteralakzat és az ügynök teljes tartománynevét is.</span><span class="sxs-lookup"><span data-stu-id="1e72c-107">You can view the properties of a container service, which include state, number of master and agents, and fully qualified domain name of master and agent.</span></span>

## <span data-ttu-id="1e72c-108">Példák</span><span class="sxs-lookup"><span data-stu-id="1e72c-108">EXAMPLES</span></span>

### <span data-ttu-id="1e72c-109">Példa 1: tároló szolgáltatás beszerzése</span><span class="sxs-lookup"><span data-stu-id="1e72c-109">Example 1: Get a container service</span></span>
```
PS C:\> Get-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="1e72c-110">Ez a parancs CSResourceGroup17 nevű tároló szolgáltatást kap.</span><span class="sxs-lookup"><span data-stu-id="1e72c-110">This command gets a container service named CSResourceGroup17.</span></span>

## <span data-ttu-id="1e72c-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1e72c-111">PARAMETERS</span></span>

### <span data-ttu-id="1e72c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e72c-112">-DefaultProfile</span></span>
<span data-ttu-id="1e72c-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1e72c-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1e72c-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1e72c-114">-Name</span></span>
<span data-ttu-id="1e72c-115">Annak a tároló szolgáltatásnak a neve, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="1e72c-115">Specifies the name of the container service that this cmdlet gets.</span></span>

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

### <span data-ttu-id="1e72c-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e72c-116">-ResourceGroupName</span></span>
<span data-ttu-id="1e72c-117">Annak a tároló szolgáltatásnak az erőforrás csoportját adja meg, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="1e72c-117">Specifies the resource group of the container service that this cmdlet gets.</span></span>

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

### <span data-ttu-id="1e72c-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e72c-118">CommonParameters</span></span>
<span data-ttu-id="1e72c-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1e72c-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e72c-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e72c-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e72c-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1e72c-121">INPUTS</span></span>

### <span data-ttu-id="1e72c-122">Nincs</span><span class="sxs-lookup"><span data-stu-id="1e72c-122">None</span></span>
<span data-ttu-id="1e72c-123">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="1e72c-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1e72c-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1e72c-124">OUTPUTS</span></span>

### <span data-ttu-id="1e72c-125">Microsoft. Azure. commands. számítási. Automation. models. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="1e72c-125">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="1e72c-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1e72c-126">NOTES</span></span>

## <span data-ttu-id="1e72c-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1e72c-127">RELATED LINKS</span></span>

[<span data-ttu-id="1e72c-128">Új – AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="1e72c-128">New-AzureRmContainerService</span></span>](./New-AzureRmContainerService.md)

[<span data-ttu-id="1e72c-129">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="1e72c-129">Remove-AzureRmContainerService</span></span>](./Remove-AzureRmContainerService.md)

[<span data-ttu-id="1e72c-130">Update-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="1e72c-130">Update-AzureRmContainerService</span></span>](./Update-AzureRmContainerService.md)


