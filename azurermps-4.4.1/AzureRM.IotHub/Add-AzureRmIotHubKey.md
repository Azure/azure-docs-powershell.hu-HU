---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Add-AzureRmIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Add-AzureRmIotHubKey.md
ms.openlocfilehash: f7bbe0c37d03a6db372c6c70da021160060a542a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501835"
---
# <span data-ttu-id="551a6-101">Add-AzureRmIotHubKey</span><span class="sxs-lookup"><span data-stu-id="551a6-101">Add-AzureRmIotHubKey</span></span>

## <span data-ttu-id="551a6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="551a6-102">SYNOPSIS</span></span>
<span data-ttu-id="551a6-103">Létrehoz egy IotHub kulcsot.</span><span class="sxs-lookup"><span data-stu-id="551a6-103">Creates an IotHub Key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="551a6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="551a6-104">SYNTAX</span></span>

```
Add-AzureRmIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [[-PrimaryKey] <String>] [[-SecondaryKey] <String>] [-Rights] <PSAccessRights>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="551a6-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="551a6-105">DESCRIPTION</span></span>
<span data-ttu-id="551a6-106">A megadott IotHub kulcsát hozza létre.</span><span class="sxs-lookup"><span data-stu-id="551a6-106">Creates a Key for the provided IotHub.</span></span>
<span data-ttu-id="551a6-107">A saját nevek nem egyediek, és körültekintően kell kezelni őket.</span><span class="sxs-lookup"><span data-stu-id="551a6-107">KeyNames are not unique and need to be managed carefully.</span></span>

## <span data-ttu-id="551a6-108">Példák</span><span class="sxs-lookup"><span data-stu-id="551a6-108">EXAMPLES</span></span>

### <span data-ttu-id="551a6-109">Példa 1 kulcs felvétele egy IotHub</span><span class="sxs-lookup"><span data-stu-id="551a6-109">Example 1 Add a Key to an IotHub</span></span>
```
PS C:\> Add-AzureRmIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "newkey" -PrimaryKey "primarykey" -SecondaryKey "secondarykey" -Rights RegistryRead
```

<span data-ttu-id="551a6-110">A iothub "myiothub" nevű "Mykey" nevű kulcs létrehozása RegistryRead engedélyekkel.</span><span class="sxs-lookup"><span data-stu-id="551a6-110">Creates a key named "mykey" for the iothub "myiothub" with RegistryRead permissions.</span></span>

## <span data-ttu-id="551a6-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="551a6-111">PARAMETERS</span></span>

### <span data-ttu-id="551a6-112">-Kulcsnév</span><span class="sxs-lookup"><span data-stu-id="551a6-112">-KeyName</span></span>
<span data-ttu-id="551a6-113">A kulcs neve</span><span class="sxs-lookup"><span data-stu-id="551a6-113">Name of the Key</span></span>

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

### <span data-ttu-id="551a6-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="551a6-114">-Name</span></span>
<span data-ttu-id="551a6-115">A IotHub neve</span><span class="sxs-lookup"><span data-stu-id="551a6-115">Name of the IotHub</span></span>

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

### <span data-ttu-id="551a6-116">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="551a6-116">-PrimaryKey</span></span>
<span data-ttu-id="551a6-117">Az elsődleges kulcs</span><span class="sxs-lookup"><span data-stu-id="551a6-117">The primary key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="551a6-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="551a6-118">-ResourceGroupName</span></span>
<span data-ttu-id="551a6-119">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="551a6-119">Resource Group Name</span></span>

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

### <span data-ttu-id="551a6-120">– Jogok</span><span class="sxs-lookup"><span data-stu-id="551a6-120">-Rights</span></span>
<span data-ttu-id="551a6-121">A IOTHub engedélyei</span><span class="sxs-lookup"><span data-stu-id="551a6-121">The permissions for this IOTHub</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSAccessRights
Parameter Sets: (All)
Aliases: 
Accepted values: RegistryRead, RegistryWrite, ServiceConnect, DeviceConnect

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="551a6-122">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="551a6-122">-SecondaryKey</span></span>
<span data-ttu-id="551a6-123">A másodlagos kulcs</span><span class="sxs-lookup"><span data-stu-id="551a6-123">The Secondary Key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="551a6-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="551a6-124">-Confirm</span></span>
<span data-ttu-id="551a6-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="551a6-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="551a6-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="551a6-126">-WhatIf</span></span>
<span data-ttu-id="551a6-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="551a6-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="551a6-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="551a6-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="551a6-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="551a6-129">-DefaultProfile</span></span>
<span data-ttu-id="551a6-130">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="551a6-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="551a6-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="551a6-131">CommonParameters</span></span>
<span data-ttu-id="551a6-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="551a6-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="551a6-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="551a6-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="551a6-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="551a6-134">INPUTS</span></span>

### <span data-ttu-id="551a6-135">System. String</span><span class="sxs-lookup"><span data-stu-id="551a6-135">System.String</span></span>
<span data-ttu-id="551a6-136">Microsoft. Azure. Command. Management. IotHub. models. PSAccessRights</span><span class="sxs-lookup"><span data-stu-id="551a6-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSAccessRights</span></span>

## <span data-ttu-id="551a6-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="551a6-137">OUTPUTS</span></span>

### <span data-ttu-id="551a6-138">Microsoft. Azure. Command. Management. IotHub. models. PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="551a6-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>
<span data-ttu-id="551a6-139">System. Collections. Generic. list \` 1 \[ \[ Microsoft. Azure. Command. Management. IotHub. models. PSSharedAccessSignatureAuthorizationRule, Microsoft. Azure. commands. IotHub, Version = 1.0.0.0, Culture = semleges, PublicKeyToken = null\]\]</span><span class="sxs-lookup"><span data-stu-id="551a6-139">System.Collections.Generic.List\`1\[\[Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule, Microsoft.Azure.Commands.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null\]\]</span></span>

## <span data-ttu-id="551a6-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="551a6-140">NOTES</span></span>

## <span data-ttu-id="551a6-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="551a6-141">RELATED LINKS</span></span>

