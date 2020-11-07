---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: AFF75E0B-CB88-45ED-9067-7F43E2BA485C
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azcontainerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzContainerService.md
ms.openlocfilehash: 1a0daa4bf336ba970c12c24db3d5aab73641aaea
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844665"
---
# <span data-ttu-id="7696f-101">Get-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="7696f-101">Get-AzContainerService</span></span>

## <span data-ttu-id="7696f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7696f-102">SYNOPSIS</span></span>
<span data-ttu-id="7696f-103">Tároló szolgáltatást kap.</span><span class="sxs-lookup"><span data-stu-id="7696f-103">Gets a container service.</span></span>

## <span data-ttu-id="7696f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7696f-104">SYNTAX</span></span>

```
Get-AzContainerService [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7696f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7696f-105">DESCRIPTION</span></span>
<span data-ttu-id="7696f-106">A **Get-AzContainerService** parancsmag tároló szolgáltatást kap.</span><span class="sxs-lookup"><span data-stu-id="7696f-106">The **Get-AzContainerService** cmdlet gets a container service.</span></span>
<span data-ttu-id="7696f-107">Megtekintheti a tároló szolgáltatás tulajdonságait, amely tartalmazza az állapotot, a mesteralakzatok számát és az ügynököket, valamint a mesteralakzat és az ügynök teljes tartománynevét is.</span><span class="sxs-lookup"><span data-stu-id="7696f-107">You can view the properties of a container service, which include state, number of master and agents, and fully qualified domain name of master and agent.</span></span>

## <span data-ttu-id="7696f-108">Példák</span><span class="sxs-lookup"><span data-stu-id="7696f-108">EXAMPLES</span></span>

### <span data-ttu-id="7696f-109">Példa 1: tároló szolgáltatás beszerzése</span><span class="sxs-lookup"><span data-stu-id="7696f-109">Example 1: Get a container service</span></span>
```
PS C:\> Get-AzContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="7696f-110">Ez a parancs CSResourceGroup17 nevű tároló szolgáltatást kap.</span><span class="sxs-lookup"><span data-stu-id="7696f-110">This command gets a container service named CSResourceGroup17.</span></span>

## <span data-ttu-id="7696f-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7696f-111">PARAMETERS</span></span>

### <span data-ttu-id="7696f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7696f-112">-DefaultProfile</span></span>
<span data-ttu-id="7696f-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7696f-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7696f-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7696f-114">-Name</span></span>
<span data-ttu-id="7696f-115">Annak a tároló szolgáltatásnak a neve, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="7696f-115">Specifies the name of the container service that this cmdlet gets.</span></span>

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

### <span data-ttu-id="7696f-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7696f-116">-ResourceGroupName</span></span>
<span data-ttu-id="7696f-117">Annak a tároló szolgáltatásnak az erőforrás csoportját adja meg, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="7696f-117">Specifies the resource group of the container service that this cmdlet gets.</span></span>

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

### <span data-ttu-id="7696f-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7696f-118">CommonParameters</span></span>
<span data-ttu-id="7696f-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7696f-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7696f-120">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7696f-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7696f-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7696f-121">INPUTS</span></span>

### <span data-ttu-id="7696f-122">Nincs</span><span class="sxs-lookup"><span data-stu-id="7696f-122">None</span></span>
<span data-ttu-id="7696f-123">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="7696f-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7696f-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7696f-124">OUTPUTS</span></span>

### <span data-ttu-id="7696f-125">Microsoft. Azure. commands. számítási. Automation. models. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="7696f-125">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="7696f-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7696f-126">NOTES</span></span>

## <span data-ttu-id="7696f-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7696f-127">RELATED LINKS</span></span>

[<span data-ttu-id="7696f-128">Új – AzContainerService</span><span class="sxs-lookup"><span data-stu-id="7696f-128">New-AzContainerService</span></span>](./New-AzContainerService.md)

[<span data-ttu-id="7696f-129">Remove-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="7696f-129">Remove-AzContainerService</span></span>](./Remove-AzContainerService.md)

[<span data-ttu-id="7696f-130">Update-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="7696f-130">Update-AzContainerService</span></span>](./Update-AzContainerService.md)


