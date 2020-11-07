---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/get-azurermiothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHub.md
ms.openlocfilehash: 80b629fe3d5ff5e028b73b22af95243849ecede7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672642"
---
# <span data-ttu-id="a8570-101">Get-AzureRmIotHub</span><span class="sxs-lookup"><span data-stu-id="a8570-101">Get-AzureRmIotHub</span></span>

## <span data-ttu-id="a8570-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a8570-102">SYNOPSIS</span></span>
<span data-ttu-id="a8570-103">Információt kap az előfizetésben szereplő IotHubs.</span><span class="sxs-lookup"><span data-stu-id="a8570-103">Gets information about the IotHubs in a subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a8570-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a8570-104">SYNTAX</span></span>

### <span data-ttu-id="a8570-105">ListIotHubsByResourceGroup (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a8570-105">ListIotHubsByResourceGroup (Default)</span></span>
```
Get-AzureRmIotHub [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a8570-106">GetIotHubByName</span><span class="sxs-lookup"><span data-stu-id="a8570-106">GetIotHubByName</span></span>
```
Get-AzureRmIotHub [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a8570-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="a8570-107">DESCRIPTION</span></span>
<span data-ttu-id="a8570-108">Információt kap az előfizetésben szereplő IotHubs.</span><span class="sxs-lookup"><span data-stu-id="a8570-108">Gets information about the IotHubs in a subscription.</span></span>
<span data-ttu-id="a8570-109">Egy előfizetésben megtekintheti az összes IotHub-példányt, vagy szűrheti az eredményeket egy erőforráscsoport vagy egy adott IotHub nevével.</span><span class="sxs-lookup"><span data-stu-id="a8570-109">You can view all IotHub instances in a subscription, or filter your results by a resource group or a particular IotHub Name.</span></span>

## <span data-ttu-id="a8570-110">Példák</span><span class="sxs-lookup"><span data-stu-id="a8570-110">EXAMPLES</span></span>

### <span data-ttu-id="a8570-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="a8570-111">Example 1</span></span>
```
PS C:\> Get-AzureRmIotHub
```

<span data-ttu-id="a8570-112">Az előfizetésben lévő összes IotHubs kapja.</span><span class="sxs-lookup"><span data-stu-id="a8570-112">Gets all the IotHubs in the subscription.</span></span>

### <span data-ttu-id="a8570-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="a8570-113">Example 2</span></span>
```
PS C:\> Get-AzureRmIotHub -ResourceGroupName "myresourcegroup"
```

<span data-ttu-id="a8570-114">Az előfizetéshez tartozó összes IotHubs megkapja az "myresourcegroup" nevű resourcegroup.</span><span class="sxs-lookup"><span data-stu-id="a8570-114">Gets all the IotHubs in the subscription belonging to the resourcegroup named "myresourcegroup".</span></span>

### <span data-ttu-id="a8570-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="a8570-115">Example 3</span></span>
```
PS C:\> Get-AzureRmIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="a8570-116">Információt kap a "myiothub" nevű IotHub.</span><span class="sxs-lookup"><span data-stu-id="a8570-116">Gets information about the IotHub named "myiothub".</span></span>

## <span data-ttu-id="a8570-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a8570-117">PARAMETERS</span></span>

### <span data-ttu-id="a8570-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8570-118">-DefaultProfile</span></span>
<span data-ttu-id="a8570-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="a8570-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a8570-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a8570-120">-Name</span></span>
<span data-ttu-id="a8570-121">A IotHub neve</span><span class="sxs-lookup"><span data-stu-id="a8570-121">Name of the IotHub</span></span>

```yaml
Type: String
Parameter Sets: GetIotHubByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8570-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8570-122">-ResourceGroupName</span></span>
<span data-ttu-id="a8570-123">A ResourceGroup neve</span><span class="sxs-lookup"><span data-stu-id="a8570-123">Name of the ResourceGroup</span></span>

```yaml
Type: String
Parameter Sets: ListIotHubsByResourceGroup
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetIotHubByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8570-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8570-124">CommonParameters</span></span>
<span data-ttu-id="a8570-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a8570-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8570-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8570-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8570-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a8570-127">INPUTS</span></span>

### <span data-ttu-id="a8570-128">System. String</span><span class="sxs-lookup"><span data-stu-id="a8570-128">System.String</span></span>

## <span data-ttu-id="a8570-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a8570-129">OUTPUTS</span></span>

### <span data-ttu-id="a8570-130">Microsoft. Azure. Command. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="a8570-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>
<span data-ttu-id="a8570-131">System. Collections. Generic. list \` 1 \[ \[ Microsoft. Azure. Command. Management. IotHub. models. PSIotHub, Microsoft. Azure. commands. IotHub, Version = 1.0.0.0, Culture = semleges, PublicKeyToken = null\]\]</span><span class="sxs-lookup"><span data-stu-id="a8570-131">System.Collections.Generic.List\`1\[\[Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub, Microsoft.Azure.Commands.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null\]\]</span></span>

## <span data-ttu-id="a8570-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a8570-132">NOTES</span></span>

## <span data-ttu-id="a8570-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a8570-133">RELATED LINKS</span></span>

