---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/new-azurermdatafactorygatewayauthkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryGatewayAuthKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryGatewayAuthKey.md
ms.openlocfilehash: b7f435090c0ff5c421df7d8d3e885f67456f9af0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679856"
---
# <span data-ttu-id="4675d-101">New-AzureRmDataFactoryGatewayAuthKey</span><span class="sxs-lookup"><span data-stu-id="4675d-101">New-AzureRmDataFactoryGatewayAuthKey</span></span>

## <span data-ttu-id="4675d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4675d-102">SYNOPSIS</span></span>
<span data-ttu-id="4675d-103">Hitelesítő kulcs létrehozása Azure Data Factory átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="4675d-103">Creates auth key for an Azure Data Factory Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4675d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4675d-104">SYNTAX</span></span>

### <span data-ttu-id="4675d-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4675d-105">ByFactoryName (Default)</span></span>
```
New-AzureRmDataFactoryGatewayAuthKey [-DataFactoryName] <String> [-GatewayName] <String> [-KeyName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4675d-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="4675d-106">ByFactoryObject</span></span>
```
New-AzureRmDataFactoryGatewayAuthKey [-InputObject] <PSDataFactory> [-GatewayName] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4675d-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="4675d-107">DESCRIPTION</span></span>
<span data-ttu-id="4675d-108">A **New-AzureRmDataFactoryGatewayAuthKey** parancsmag átjáró-hitelesítési kulcsot hoz létre egy megadott Azure Data Factory átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="4675d-108">The **New-AzureRmDataFactoryGatewayAuthKey** cmdlet creates gateway auth key for a specified Azure Data Factory gateway.</span></span>
<span data-ttu-id="4675d-109">Ezzel a kulccsal regisztrálja az átjárót egy Felhőbeli szolgáltatással.</span><span class="sxs-lookup"><span data-stu-id="4675d-109">You register the gateway with a cloud service by using this key.</span></span>

## <span data-ttu-id="4675d-110">Példák</span><span class="sxs-lookup"><span data-stu-id="4675d-110">EXAMPLES</span></span>

### <span data-ttu-id="4675d-111">Példa 1: az Key1-hoz létrehoz egy átjáró hitelesítő kulcsot.</span><span class="sxs-lookup"><span data-stu-id="4675d-111">Example 1: Creates a gateway auth key for Key1</span></span>
```
PS C:\> New-AzureRmDataFactoryGatewayAuthKey -ResourceGroup ADFResource -GatewayName 'MyGateway' -DataFactoryName MyADF -KeyName key1
Key1 : DMG@632e739e-1053-4070-9102-8591f067526e@41fcbc45-c594-4152-a8f1-fcbcd6452aea@wu@BH0EV9hu/o2IYGQzfYYD203XhdS6Tty
       fkYwYFbG6wBU=
Key2 :
```

<span data-ttu-id="4675d-112">Ez a parancs létrehoz egy Key1 az MyGateway nevű adatgyári átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="4675d-112">This command creates a gateway auth key of Key1 for the data factory gateway named MyGateway.</span></span>

## <span data-ttu-id="4675d-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4675d-113">PARAMETERS</span></span>

### <span data-ttu-id="4675d-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="4675d-114">-DataFactoryName</span></span>
<span data-ttu-id="4675d-115">Az adatgyári név.</span><span class="sxs-lookup"><span data-stu-id="4675d-115">The data factory name.</span></span>

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

### <span data-ttu-id="4675d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4675d-116">-DefaultProfile</span></span>
<span data-ttu-id="4675d-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="4675d-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4675d-118">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="4675d-118">-GatewayName</span></span>
<span data-ttu-id="4675d-119">Az adatgyári átjáró neve.</span><span class="sxs-lookup"><span data-stu-id="4675d-119">The data factory gateway name.</span></span>

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

### <span data-ttu-id="4675d-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4675d-120">-InputObject</span></span>
<span data-ttu-id="4675d-121">Az Data Factory objektum</span><span class="sxs-lookup"><span data-stu-id="4675d-121">The data factory object</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: DataFactory

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4675d-122">-Kulcsnév</span><span class="sxs-lookup"><span data-stu-id="4675d-122">-KeyName</span></span>
<span data-ttu-id="4675d-123">Az újragenerálni kívánt átjáró hitelesítő kulcs neve "key1" vagy "azonosító2".</span><span class="sxs-lookup"><span data-stu-id="4675d-123">The name of gateway auth key to be regenerated, either 'key1' or 'key2'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: key1, key2

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4675d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4675d-124">-ResourceGroupName</span></span>
<span data-ttu-id="4675d-125">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="4675d-125">The resource group name.</span></span>

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

### <span data-ttu-id="4675d-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4675d-126">-Confirm</span></span>
<span data-ttu-id="4675d-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4675d-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4675d-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4675d-128">-WhatIf</span></span>
<span data-ttu-id="4675d-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4675d-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4675d-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4675d-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4675d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4675d-131">CommonParameters</span></span>
<span data-ttu-id="4675d-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4675d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4675d-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4675d-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4675d-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4675d-134">INPUTS</span></span>

### <span data-ttu-id="4675d-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="4675d-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>
<span data-ttu-id="4675d-136">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="4675d-136">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="4675d-137">System. String</span><span class="sxs-lookup"><span data-stu-id="4675d-137">System.String</span></span>

## <span data-ttu-id="4675d-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4675d-138">OUTPUTS</span></span>

### <span data-ttu-id="4675d-139">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGatewayAuthKey</span><span class="sxs-lookup"><span data-stu-id="4675d-139">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGatewayAuthKey</span></span>

## <span data-ttu-id="4675d-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4675d-140">NOTES</span></span>
* <span data-ttu-id="4675d-141">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak</span><span class="sxs-lookup"><span data-stu-id="4675d-141">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="4675d-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4675d-142">RELATED LINKS</span></span>

<span data-ttu-id="4675d-143">[Új – AzureRmDataFactoryGateway](./New-AzureRmDataFactoryGateway.md) 
 [Get-AzureRmDataFactoryGatewayAuthKey](./Get-AzureRmDataFactoryGatewayAuthKey.md)</span><span class="sxs-lookup"><span data-stu-id="4675d-143">[New-AzureRmDataFactoryGateway](./New-AzureRmDataFactoryGateway.md)
[Get-AzureRmDataFactoryGatewayAuthKey](./Get-AzureRmDataFactoryGatewayAuthKey.md)</span></span>

