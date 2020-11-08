---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/update-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHub.md
ms.openlocfilehash: 3ba9706c452c293dea6ad6a0e23a51ccb03ada9c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181891"
---
# <span data-ttu-id="e2f27-101">Update-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="e2f27-101">Update-AzIotHub</span></span>

## <span data-ttu-id="e2f27-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e2f27-102">SYNOPSIS</span></span>
<span data-ttu-id="e2f27-103">Az Azure IoT-hub frissítése</span><span class="sxs-lookup"><span data-stu-id="e2f27-103">Update an Azure IoT Hub.</span></span>

## <span data-ttu-id="e2f27-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e2f27-104">SYNTAX</span></span>

```
Update-AzIotHub -ResourceGroupName <String> -Name <String> -Tag <Hashtable> [-Reset]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2f27-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e2f27-105">DESCRIPTION</span></span>
<span data-ttu-id="e2f27-106">Frissítheti egy IotHub címkék tulajdonságát.</span><span class="sxs-lookup"><span data-stu-id="e2f27-106">You can update the tags properties of an IotHub.</span></span>

## <span data-ttu-id="e2f27-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e2f27-107">EXAMPLES</span></span>

### <span data-ttu-id="e2f27-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e2f27-108">Example 1</span></span>
```
PS C:\> Update-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -Tag @tags

Id             : /subscriptions/91d1xxxx-xxxx-xxxx-xxxx-xxxxxxxxddc0/resourceGroups/myresourcegroup/providers/Microsoft.De
                 vices/IotHubs/myiotdps
Name           : myiotdps
Type           : Microsoft.Devices/IotHubs
Location       : East US
Tags           : {[k1, v1]}
Properties     : Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties
Sku            : Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubSkuInfo
```

<span data-ttu-id="e2f27-109">" @tags " Hozzáadása egy Azure IoT-hub "myiotdps" címkéhez</span><span class="sxs-lookup"><span data-stu-id="e2f27-109">Add "@tags" to the Tag of an Azure IoT Hub "myiotdps".</span></span>

## <span data-ttu-id="e2f27-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e2f27-110">PARAMETERS</span></span>

### <span data-ttu-id="e2f27-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2f27-111">-DefaultProfile</span></span>
<span data-ttu-id="e2f27-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e2f27-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2f27-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e2f27-113">-Name</span></span>
<span data-ttu-id="e2f27-114">A IOT-központ neve</span><span class="sxs-lookup"><span data-stu-id="e2f27-114">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2f27-115">-Reset</span><span class="sxs-lookup"><span data-stu-id="e2f27-115">-Reset</span></span>
<span data-ttu-id="e2f27-116">IoTHub-címkék visszaállítása</span><span class="sxs-lookup"><span data-stu-id="e2f27-116">Reset IoTHub Tags</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2f27-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2f27-117">-ResourceGroupName</span></span>
<span data-ttu-id="e2f27-118">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="e2f27-118">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2f27-119">-Címke</span><span class="sxs-lookup"><span data-stu-id="e2f27-119">-Tag</span></span>
<span data-ttu-id="e2f27-120">IoTHub-címke gyűjteménye</span><span class="sxs-lookup"><span data-stu-id="e2f27-120">IoTHub Tag collection</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2f27-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e2f27-121">-Confirm</span></span>
<span data-ttu-id="e2f27-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e2f27-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2f27-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2f27-123">-WhatIf</span></span>
<span data-ttu-id="e2f27-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e2f27-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2f27-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e2f27-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2f27-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2f27-126">CommonParameters</span></span>
<span data-ttu-id="e2f27-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e2f27-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2f27-128">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2f27-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2f27-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e2f27-129">INPUTS</span></span>

### <span data-ttu-id="e2f27-130">System. String</span><span class="sxs-lookup"><span data-stu-id="e2f27-130">System.String</span></span>

## <span data-ttu-id="e2f27-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e2f27-131">OUTPUTS</span></span>

### <span data-ttu-id="e2f27-132">Microsoft. Azure. Command. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="e2f27-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="e2f27-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e2f27-133">NOTES</span></span>

## <span data-ttu-id="e2f27-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e2f27-134">RELATED LINKS</span></span>
