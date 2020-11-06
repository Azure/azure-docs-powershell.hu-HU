---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryGatewayAuthKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryGatewayAuthKey.md
ms.openlocfilehash: 0e6940a49e4b3a284643bd9353d579213b793d2b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497100"
---
# <span data-ttu-id="48678-101">New-AzureRmDataFactoryGatewayAuthKey</span><span class="sxs-lookup"><span data-stu-id="48678-101">New-AzureRmDataFactoryGatewayAuthKey</span></span>

## <span data-ttu-id="48678-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="48678-102">SYNOPSIS</span></span>
<span data-ttu-id="48678-103">Hitelesítő kulcs létrehozása Azure Data Factory átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="48678-103">Creates auth key for an Azure Data Factory Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="48678-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="48678-104">SYNTAX</span></span>

### <span data-ttu-id="48678-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="48678-105">ByFactoryName (Default)</span></span>
```
New-AzureRmDataFactoryGatewayAuthKey [-DataFactoryName] <String> [-GatewayName] <String> [-KeyName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="48678-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="48678-106">ByFactoryObject</span></span>
```
New-AzureRmDataFactoryGatewayAuthKey -InputObject <PSDataFactory> [-GatewayName] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="48678-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="48678-107">DESCRIPTION</span></span>
<span data-ttu-id="48678-108">A **New-AzureRmDataFactoryGatewayAuthKey** parancsmag átjáró-hitelesítési kulcsot hoz létre egy megadott Azure Data Factory átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="48678-108">The **New-AzureRmDataFactoryGatewayAuthKey** cmdlet creates gateway auth key for a specified Azure Data Factory gateway.</span></span>
<span data-ttu-id="48678-109">Ezzel a kulccsal regisztrálja az átjárót egy Felhőbeli szolgáltatással.</span><span class="sxs-lookup"><span data-stu-id="48678-109">You register the gateway with a cloud service by using this key.</span></span>

## <span data-ttu-id="48678-110">Példák</span><span class="sxs-lookup"><span data-stu-id="48678-110">EXAMPLES</span></span>

### <span data-ttu-id="48678-111">Példa 1: az Key1-hoz létrehoz egy átjáró hitelesítő kulcsot.</span><span class="sxs-lookup"><span data-stu-id="48678-111">Example 1: Creates a gateway auth key for Key1</span></span>
```
PS C:\> New-AzureRmDataFactoryGatewayAuthKey -ResourceGroup ADFResource -GatewayName 'MyGateway' -DataFactoryName MyADF -KeyName key1
Key1 : DMG@632e739e-1053-4070-9102-8591f067526e@41fcbc45-c594-4152-a8f1-fcbcd6452aea@wu@BH0EV9hu/o2IYGQzfYYD203XhdS6Tty
       fkYwYFbG6wBU=
Key2 :
```

<span data-ttu-id="48678-112">Ez a parancs létrehoz egy Key1 az MyGateway nevű adatgyári átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="48678-112">This command creates a gateway auth key of Key1 for the data factory gateway named MyGateway.</span></span>

## <span data-ttu-id="48678-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="48678-113">PARAMETERS</span></span>

### <span data-ttu-id="48678-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="48678-114">-DataFactoryName</span></span>
<span data-ttu-id="48678-115">Az adatgyári név.</span><span class="sxs-lookup"><span data-stu-id="48678-115">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48678-116">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="48678-116">-GatewayName</span></span>
<span data-ttu-id="48678-117">Az adatgyári átjáró neve.</span><span class="sxs-lookup"><span data-stu-id="48678-117">The data factory gateway name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48678-118">-Kulcsnév</span><span class="sxs-lookup"><span data-stu-id="48678-118">-KeyName</span></span>
<span data-ttu-id="48678-119">Az újragenerálni kívánt átjáró hitelesítő kulcs neve "key1" vagy "azonosító2".</span><span class="sxs-lookup"><span data-stu-id="48678-119">The name of gateway auth key to be regenerated, either 'key1' or 'key2'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48678-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48678-120">-ResourceGroupName</span></span>
<span data-ttu-id="48678-121">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="48678-121">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48678-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="48678-122">-Confirm</span></span>
<span data-ttu-id="48678-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="48678-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48678-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48678-124">-DefaultProfile</span></span>
<span data-ttu-id="48678-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="48678-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="48678-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="48678-126">-InputObject</span></span>
<span data-ttu-id="48678-127">Az Data Factory objektum.</span><span class="sxs-lookup"><span data-stu-id="48678-127">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: DataFactory

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="48678-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48678-128">-WhatIf</span></span>
<span data-ttu-id="48678-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="48678-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="48678-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="48678-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48678-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48678-131">CommonParameters</span></span>
<span data-ttu-id="48678-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="48678-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48678-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48678-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48678-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="48678-134">INPUTS</span></span>

### <span data-ttu-id="48678-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="48678-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>
<span data-ttu-id="48678-136">System. String</span><span class="sxs-lookup"><span data-stu-id="48678-136">System.String</span></span>

## <span data-ttu-id="48678-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="48678-137">OUTPUTS</span></span>

### <span data-ttu-id="48678-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGatewayAuthKey</span><span class="sxs-lookup"><span data-stu-id="48678-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGatewayAuthKey</span></span>

## <span data-ttu-id="48678-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="48678-139">NOTES</span></span>
* <span data-ttu-id="48678-140">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak</span><span class="sxs-lookup"><span data-stu-id="48678-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="48678-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="48678-141">RELATED LINKS</span></span>

<span data-ttu-id="48678-142">[Új – AzureRmDataFactoryGateway](./New-AzureRmDataFactoryGateway.md) 
 [Get-AzureRmDataFactoryGatewayAuthKey](./Get-AzureRmDataFactoryGatewayAuthKey.md)</span><span class="sxs-lookup"><span data-stu-id="48678-142">[New-AzureRmDataFactoryGateway](./New-AzureRmDataFactoryGateway.md)
[Get-AzureRmDataFactoryGatewayAuthKey](./Get-AzureRmDataFactoryGatewayAuthKey.md)</span></span>

