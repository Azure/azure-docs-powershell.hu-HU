---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/add-azurermiothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Add-AzureRmIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Add-AzureRmIotHubKey.md
ms.openlocfilehash: 379aaa360776291515f1848cd48b24e88be23ef6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496087"
---
# <span data-ttu-id="23cbf-101">Add-AzureRmIotHubKey</span><span class="sxs-lookup"><span data-stu-id="23cbf-101">Add-AzureRmIotHubKey</span></span>

## <span data-ttu-id="23cbf-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="23cbf-102">SYNOPSIS</span></span>
<span data-ttu-id="23cbf-103">Létrehoz egy IotHub kulcsot.</span><span class="sxs-lookup"><span data-stu-id="23cbf-103">Creates an IotHub Key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="23cbf-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="23cbf-104">SYNTAX</span></span>

```
Add-AzureRmIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String> [-PrimaryKey <String>]
 [-SecondaryKey <String>] -Rights <PSAccessRights> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23cbf-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="23cbf-105">DESCRIPTION</span></span>
<span data-ttu-id="23cbf-106">A megadott IotHub kulcsát hozza létre.</span><span class="sxs-lookup"><span data-stu-id="23cbf-106">Creates a Key for the provided IotHub.</span></span>
<span data-ttu-id="23cbf-107">A saját nevek nem egyediek, és körültekintően kell kezelni őket.</span><span class="sxs-lookup"><span data-stu-id="23cbf-107">KeyNames are not unique and need to be managed carefully.</span></span>

## <span data-ttu-id="23cbf-108">Példák</span><span class="sxs-lookup"><span data-stu-id="23cbf-108">EXAMPLES</span></span>

### <span data-ttu-id="23cbf-109">Példa 1 kulcs felvétele egy IotHub</span><span class="sxs-lookup"><span data-stu-id="23cbf-109">Example 1 Add a Key to an IotHub</span></span>
```
PS C:\> Add-AzureRmIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "newkey" -PrimaryKey "primarykey" -SecondaryKey "secondarykey" -Rights RegistryRead
```

<span data-ttu-id="23cbf-110">A iothub "myiothub" nevű "Mykey" nevű kulcs létrehozása RegistryRead engedélyekkel.</span><span class="sxs-lookup"><span data-stu-id="23cbf-110">Creates a key named "mykey" for the iothub "myiothub" with RegistryRead permissions.</span></span>

## <span data-ttu-id="23cbf-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="23cbf-111">PARAMETERS</span></span>

### <span data-ttu-id="23cbf-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23cbf-112">-DefaultProfile</span></span>
<span data-ttu-id="23cbf-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="23cbf-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23cbf-114">-Kulcsnév</span><span class="sxs-lookup"><span data-stu-id="23cbf-114">-KeyName</span></span>
<span data-ttu-id="23cbf-115">A kulcs neve</span><span class="sxs-lookup"><span data-stu-id="23cbf-115">Name of the Key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23cbf-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="23cbf-116">-Name</span></span>
<span data-ttu-id="23cbf-117">A IotHub neve</span><span class="sxs-lookup"><span data-stu-id="23cbf-117">Name of the IotHub</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23cbf-118">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="23cbf-118">-PrimaryKey</span></span>
<span data-ttu-id="23cbf-119">Az elsődleges kulcs</span><span class="sxs-lookup"><span data-stu-id="23cbf-119">The primary key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23cbf-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23cbf-120">-ResourceGroupName</span></span>
<span data-ttu-id="23cbf-121">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="23cbf-121">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23cbf-122">– Jogok</span><span class="sxs-lookup"><span data-stu-id="23cbf-122">-Rights</span></span>
<span data-ttu-id="23cbf-123">A IOTHub engedélyei</span><span class="sxs-lookup"><span data-stu-id="23cbf-123">The permissions for this IOTHub</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSAccessRights
Parameter Sets: (All)
Aliases:
Accepted values: RegistryRead, RegistryWrite, ServiceConnect, DeviceConnect

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23cbf-124">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="23cbf-124">-SecondaryKey</span></span>
<span data-ttu-id="23cbf-125">A másodlagos kulcs</span><span class="sxs-lookup"><span data-stu-id="23cbf-125">The Secondary Key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23cbf-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="23cbf-126">-Confirm</span></span>
<span data-ttu-id="23cbf-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="23cbf-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23cbf-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23cbf-128">-WhatIf</span></span>
<span data-ttu-id="23cbf-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="23cbf-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23cbf-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="23cbf-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23cbf-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23cbf-131">CommonParameters</span></span>
<span data-ttu-id="23cbf-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="23cbf-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23cbf-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23cbf-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23cbf-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="23cbf-134">INPUTS</span></span>

### <span data-ttu-id="23cbf-135">System. String</span><span class="sxs-lookup"><span data-stu-id="23cbf-135">System.String</span></span>

## <span data-ttu-id="23cbf-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="23cbf-136">OUTPUTS</span></span>

### <span data-ttu-id="23cbf-137">Microsoft. Azure. Command. Management. IotHub. models. PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="23cbf-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="23cbf-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="23cbf-138">NOTES</span></span>

## <span data-ttu-id="23cbf-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="23cbf-139">RELATED LINKS</span></span>
