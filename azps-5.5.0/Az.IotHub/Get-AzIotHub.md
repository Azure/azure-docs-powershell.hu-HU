---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHub.md
ms.openlocfilehash: 0656726757584bf923d6ecaa7642aa67ff46596a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100159674"
---
# <span data-ttu-id="39e25-101">Get-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="39e25-101">Get-AzIotHub</span></span>

## <span data-ttu-id="39e25-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39e25-102">SYNOPSIS</span></span>
<span data-ttu-id="39e25-103">Információkat kap az IotHubsról egy előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="39e25-103">Gets information about the IotHubs in a subscription.</span></span>

## <span data-ttu-id="39e25-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="39e25-104">SYNTAX</span></span>

### <span data-ttu-id="39e25-105">ListIotHubsByResourceGroup (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="39e25-105">ListIotHubsByResourceGroup (Default)</span></span>
```
Get-AzIotHub [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="39e25-106">GetIotHubByName</span><span class="sxs-lookup"><span data-stu-id="39e25-106">GetIotHubByName</span></span>
```
Get-AzIotHub [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="39e25-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="39e25-107">DESCRIPTION</span></span>
<span data-ttu-id="39e25-108">Információkat kap az IotHubsról egy előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="39e25-108">Gets information about the IotHubs in a subscription.</span></span>
<span data-ttu-id="39e25-109">Megtekintheti egy előfizetés összes IotHub-példányát, vagy szűrheti az eredményeket egy erőforráscsoport vagy egy adott IotHub-név szerint.</span><span class="sxs-lookup"><span data-stu-id="39e25-109">You can view all IotHub instances in a subscription, or filter your results by a resource group or a particular IotHub Name.</span></span>

## <span data-ttu-id="39e25-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="39e25-110">EXAMPLES</span></span>

### <span data-ttu-id="39e25-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="39e25-111">Example 1</span></span>
```
PS C:\> Get-AzIotHub
```

<span data-ttu-id="39e25-112">Az előfizetésben található összes IotHubot beveszi.</span><span class="sxs-lookup"><span data-stu-id="39e25-112">Gets all the IotHubs in the subscription.</span></span>

### <span data-ttu-id="39e25-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="39e25-113">Example 2</span></span>
```
PS C:\> Get-AzIotHub -ResourceGroupName "myresourcegroup"
```

<span data-ttu-id="39e25-114">Az előfizetésben található összes IotHubot beveszi, amely a "myresourcegroup" nevű erőforráscsoporthoz tartozik.</span><span class="sxs-lookup"><span data-stu-id="39e25-114">Gets all the IotHubs in the subscription belonging to the resourcegroup named "myresourcegroup".</span></span>

### <span data-ttu-id="39e25-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="39e25-115">Example 3</span></span>
```
PS C:\> Get-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="39e25-116">Információkat kap a "myiothub" nevű IotHubról.</span><span class="sxs-lookup"><span data-stu-id="39e25-116">Gets information about the IotHub named "myiothub".</span></span>

## <span data-ttu-id="39e25-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="39e25-117">PARAMETERS</span></span>

### <span data-ttu-id="39e25-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39e25-118">-DefaultProfile</span></span>
<span data-ttu-id="39e25-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="39e25-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="39e25-120">-Name</span><span class="sxs-lookup"><span data-stu-id="39e25-120">-Name</span></span>
<span data-ttu-id="39e25-121">Az IotHub neve</span><span class="sxs-lookup"><span data-stu-id="39e25-121">Name of the IotHub</span></span>

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

### <span data-ttu-id="39e25-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39e25-122">-ResourceGroupName</span></span>
<span data-ttu-id="39e25-123">Az Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="39e25-123">Name of the ResourceGroup</span></span>

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

### <span data-ttu-id="39e25-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39e25-124">CommonParameters</span></span>
<span data-ttu-id="39e25-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39e25-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39e25-126">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39e25-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39e25-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="39e25-127">INPUTS</span></span>

### <span data-ttu-id="39e25-128">System.String</span><span class="sxs-lookup"><span data-stu-id="39e25-128">System.String</span></span>

## <span data-ttu-id="39e25-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="39e25-129">OUTPUTS</span></span>

### <span data-ttu-id="39e25-130">Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="39e25-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="39e25-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="39e25-131">NOTES</span></span>

## <span data-ttu-id="39e25-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="39e25-132">RELATED LINKS</span></span>
