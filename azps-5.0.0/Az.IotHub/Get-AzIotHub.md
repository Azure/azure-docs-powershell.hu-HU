---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHub.md
ms.openlocfilehash: 0656726757584bf923d6ecaa7642aa67ff46596a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187771"
---
# <span data-ttu-id="9503d-101">Get-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="9503d-101">Get-AzIotHub</span></span>

## <span data-ttu-id="9503d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9503d-102">SYNOPSIS</span></span>
<span data-ttu-id="9503d-103">Információt kap az előfizetésben szereplő IotHubs.</span><span class="sxs-lookup"><span data-stu-id="9503d-103">Gets information about the IotHubs in a subscription.</span></span>

## <span data-ttu-id="9503d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9503d-104">SYNTAX</span></span>

### <span data-ttu-id="9503d-105">ListIotHubsByResourceGroup (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9503d-105">ListIotHubsByResourceGroup (Default)</span></span>
```
Get-AzIotHub [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9503d-106">GetIotHubByName</span><span class="sxs-lookup"><span data-stu-id="9503d-106">GetIotHubByName</span></span>
```
Get-AzIotHub [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9503d-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="9503d-107">DESCRIPTION</span></span>
<span data-ttu-id="9503d-108">Információt kap az előfizetésben szereplő IotHubs.</span><span class="sxs-lookup"><span data-stu-id="9503d-108">Gets information about the IotHubs in a subscription.</span></span>
<span data-ttu-id="9503d-109">Egy előfizetésben megtekintheti az összes IotHub-példányt, vagy szűrheti az eredményeket egy erőforráscsoport vagy egy adott IotHub nevével.</span><span class="sxs-lookup"><span data-stu-id="9503d-109">You can view all IotHub instances in a subscription, or filter your results by a resource group or a particular IotHub Name.</span></span>

## <span data-ttu-id="9503d-110">Példák</span><span class="sxs-lookup"><span data-stu-id="9503d-110">EXAMPLES</span></span>

### <span data-ttu-id="9503d-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="9503d-111">Example 1</span></span>
```
PS C:\> Get-AzIotHub
```

<span data-ttu-id="9503d-112">Az előfizetésben lévő összes IotHubs kapja.</span><span class="sxs-lookup"><span data-stu-id="9503d-112">Gets all the IotHubs in the subscription.</span></span>

### <span data-ttu-id="9503d-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="9503d-113">Example 2</span></span>
```
PS C:\> Get-AzIotHub -ResourceGroupName "myresourcegroup"
```

<span data-ttu-id="9503d-114">Az előfizetéshez tartozó összes IotHubs megkapja az "myresourcegroup" nevű resourcegroup.</span><span class="sxs-lookup"><span data-stu-id="9503d-114">Gets all the IotHubs in the subscription belonging to the resourcegroup named "myresourcegroup".</span></span>

### <span data-ttu-id="9503d-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="9503d-115">Example 3</span></span>
```
PS C:\> Get-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="9503d-116">Információt kap a "myiothub" nevű IotHub.</span><span class="sxs-lookup"><span data-stu-id="9503d-116">Gets information about the IotHub named "myiothub".</span></span>

## <span data-ttu-id="9503d-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9503d-117">PARAMETERS</span></span>

### <span data-ttu-id="9503d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9503d-118">-DefaultProfile</span></span>
<span data-ttu-id="9503d-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="9503d-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9503d-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9503d-120">-Name</span></span>
<span data-ttu-id="9503d-121">A IotHub neve</span><span class="sxs-lookup"><span data-stu-id="9503d-121">Name of the IotHub</span></span>

```yaml
Type: System.String
Parameter Sets: GetIotHubByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9503d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9503d-122">-ResourceGroupName</span></span>
<span data-ttu-id="9503d-123">A ResourceGroup neve</span><span class="sxs-lookup"><span data-stu-id="9503d-123">Name of the ResourceGroup</span></span>

```yaml
Type: System.String
Parameter Sets: ListIotHubsByResourceGroup
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetIotHubByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9503d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9503d-124">CommonParameters</span></span>
<span data-ttu-id="9503d-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9503d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9503d-126">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9503d-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9503d-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9503d-127">INPUTS</span></span>

### <span data-ttu-id="9503d-128">System. String</span><span class="sxs-lookup"><span data-stu-id="9503d-128">System.String</span></span>

## <span data-ttu-id="9503d-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9503d-129">OUTPUTS</span></span>

### <span data-ttu-id="9503d-130">Microsoft. Azure. Command. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="9503d-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="9503d-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9503d-131">NOTES</span></span>

## <span data-ttu-id="9503d-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9503d-132">RELATED LINKS</span></span>