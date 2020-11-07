---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Get-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Get-AzIotHub.md
ms.openlocfilehash: 1076ff16005665aa81e4775507a236fe62bb0965
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843961"
---
# <span data-ttu-id="cef31-101">Get-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="cef31-101">Get-AzIotHub</span></span>

## <span data-ttu-id="cef31-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cef31-102">SYNOPSIS</span></span>
<span data-ttu-id="cef31-103">Információt kap az előfizetésben szereplő IotHubs.</span><span class="sxs-lookup"><span data-stu-id="cef31-103">Gets information about the IotHubs in a subscription.</span></span>

## <span data-ttu-id="cef31-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cef31-104">SYNTAX</span></span>

### <span data-ttu-id="cef31-105">ListIotHubsByResourceGroup (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cef31-105">ListIotHubsByResourceGroup (Default)</span></span>
```
Get-AzIotHub [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cef31-106">GetIotHubByName</span><span class="sxs-lookup"><span data-stu-id="cef31-106">GetIotHubByName</span></span>
```
Get-AzIotHub [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cef31-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="cef31-107">DESCRIPTION</span></span>
<span data-ttu-id="cef31-108">Információt kap az előfizetésben szereplő IotHubs.</span><span class="sxs-lookup"><span data-stu-id="cef31-108">Gets information about the IotHubs in a subscription.</span></span>
<span data-ttu-id="cef31-109">Egy előfizetésben megtekintheti az összes IotHub-példányt, vagy szűrheti az eredményeket egy erőforráscsoport vagy egy adott IotHub nevével.</span><span class="sxs-lookup"><span data-stu-id="cef31-109">You can view all IotHub instances in a subscription, or filter your results by a resource group or a particular IotHub Name.</span></span>

## <span data-ttu-id="cef31-110">Példák</span><span class="sxs-lookup"><span data-stu-id="cef31-110">EXAMPLES</span></span>

### <span data-ttu-id="cef31-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="cef31-111">Example 1</span></span>
```
PS C:\> Get-AzIotHub
```

<span data-ttu-id="cef31-112">Az előfizetésben lévő összes IotHubs kapja.</span><span class="sxs-lookup"><span data-stu-id="cef31-112">Gets all the IotHubs in the subscription.</span></span>

### <span data-ttu-id="cef31-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="cef31-113">Example 2</span></span>
```
PS C:\> Get-AzIotHub -ResourceGroupName "myresourcegroup"
```

<span data-ttu-id="cef31-114">Az előfizetéshez tartozó összes IotHubs megkapja az "myresourcegroup" nevű resourcegroup.</span><span class="sxs-lookup"><span data-stu-id="cef31-114">Gets all the IotHubs in the subscription belonging to the resourcegroup named "myresourcegroup".</span></span>

### <span data-ttu-id="cef31-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="cef31-115">Example 3</span></span>
```
PS C:\> Get-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="cef31-116">Információt kap a "myiothub" nevű IotHub.</span><span class="sxs-lookup"><span data-stu-id="cef31-116">Gets information about the IotHub named "myiothub".</span></span>

## <span data-ttu-id="cef31-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cef31-117">PARAMETERS</span></span>

### <span data-ttu-id="cef31-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cef31-118">-DefaultProfile</span></span>
<span data-ttu-id="cef31-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="cef31-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cef31-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="cef31-120">-Name</span></span>
<span data-ttu-id="cef31-121">A IotHub neve</span><span class="sxs-lookup"><span data-stu-id="cef31-121">Name of the IotHub</span></span>

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

### <span data-ttu-id="cef31-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cef31-122">-ResourceGroupName</span></span>
<span data-ttu-id="cef31-123">A ResourceGroup neve</span><span class="sxs-lookup"><span data-stu-id="cef31-123">Name of the ResourceGroup</span></span>

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

### <span data-ttu-id="cef31-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cef31-124">CommonParameters</span></span>
<span data-ttu-id="cef31-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cef31-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cef31-126">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cef31-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cef31-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cef31-127">INPUTS</span></span>

### <span data-ttu-id="cef31-128">System. String</span><span class="sxs-lookup"><span data-stu-id="cef31-128">System.String</span></span>

## <span data-ttu-id="cef31-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cef31-129">OUTPUTS</span></span>

### <span data-ttu-id="cef31-130">Microsoft. Azure. Command. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="cef31-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="cef31-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cef31-131">NOTES</span></span>

## <span data-ttu-id="cef31-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cef31-132">RELATED LINKS</span></span>
