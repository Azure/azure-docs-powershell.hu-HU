---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactorygatewayauthkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryGatewayAuthKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryGatewayAuthKey.md
ms.openlocfilehash: 541cedecbad563be3e1a016dd651d3e93af44d1e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847234"
---
# <span data-ttu-id="ba67e-101">New-AzDataFactoryGatewayAuthKey</span><span class="sxs-lookup"><span data-stu-id="ba67e-101">New-AzDataFactoryGatewayAuthKey</span></span>

## <span data-ttu-id="ba67e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ba67e-102">SYNOPSIS</span></span>
<span data-ttu-id="ba67e-103">Hitelesítő kulcs létrehozása Azure Data Factory átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="ba67e-103">Creates auth key for an Azure Data Factory Gateway.</span></span>

## <span data-ttu-id="ba67e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ba67e-104">SYNTAX</span></span>

### <span data-ttu-id="ba67e-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ba67e-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryGatewayAuthKey [-DataFactoryName] <String> [-GatewayName] <String> [-KeyName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ba67e-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="ba67e-106">ByFactoryObject</span></span>
```
New-AzDataFactoryGatewayAuthKey [-InputObject] <PSDataFactory> [-GatewayName] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba67e-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="ba67e-107">DESCRIPTION</span></span>
<span data-ttu-id="ba67e-108">A **New-AzDataFactoryGatewayAuthKey** parancsmag átjáró-hitelesítési kulcsot hoz létre egy megadott Azure Data Factory átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="ba67e-108">The **New-AzDataFactoryGatewayAuthKey** cmdlet creates gateway auth key for a specified Azure Data Factory gateway.</span></span>
<span data-ttu-id="ba67e-109">Ezzel a kulccsal regisztrálja az átjárót egy Felhőbeli szolgáltatással.</span><span class="sxs-lookup"><span data-stu-id="ba67e-109">You register the gateway with a cloud service by using this key.</span></span>

## <span data-ttu-id="ba67e-110">Példák</span><span class="sxs-lookup"><span data-stu-id="ba67e-110">EXAMPLES</span></span>

### <span data-ttu-id="ba67e-111">Példa 1: az Key1-hoz létrehoz egy átjáró hitelesítő kulcsot.</span><span class="sxs-lookup"><span data-stu-id="ba67e-111">Example 1: Creates a gateway auth key for Key1</span></span>
```
PS C:\> New-AzDataFactoryGatewayAuthKey -ResourceGroup ADFResource -GatewayName 'MyGateway' -DataFactoryName MyADF -KeyName key1
Key1 : DMG@632e739e-1053-4070-9102-8591f067526e@41fcbc45-c594-4152-a8f1-fcbcd6452aea@wu@BH0EV9hu/o2IYGQzfYYD203XhdS6Tty
       fkYwYFbG6wBU=
Key2 :
```

<span data-ttu-id="ba67e-112">Ez a parancs létrehoz egy Key1 az MyGateway nevű adatgyári átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="ba67e-112">This command creates a gateway auth key of Key1 for the data factory gateway named MyGateway.</span></span>

## <span data-ttu-id="ba67e-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ba67e-113">PARAMETERS</span></span>

### <span data-ttu-id="ba67e-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="ba67e-114">-DataFactoryName</span></span>
<span data-ttu-id="ba67e-115">Az adatgyári név.</span><span class="sxs-lookup"><span data-stu-id="ba67e-115">The data factory name.</span></span>

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

### <span data-ttu-id="ba67e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba67e-116">-DefaultProfile</span></span>
<span data-ttu-id="ba67e-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="ba67e-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ba67e-118">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="ba67e-118">-GatewayName</span></span>
<span data-ttu-id="ba67e-119">Az adatgyári átjáró neve.</span><span class="sxs-lookup"><span data-stu-id="ba67e-119">The data factory gateway name.</span></span>

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

### <span data-ttu-id="ba67e-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ba67e-120">-InputObject</span></span>
<span data-ttu-id="ba67e-121">Az Data Factory objektum</span><span class="sxs-lookup"><span data-stu-id="ba67e-121">The data factory object</span></span>

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

### <span data-ttu-id="ba67e-122">-Kulcsnév</span><span class="sxs-lookup"><span data-stu-id="ba67e-122">-KeyName</span></span>
<span data-ttu-id="ba67e-123">Az újragenerálni kívánt átjáró hitelesítő kulcs neve "key1" vagy "azonosító2".</span><span class="sxs-lookup"><span data-stu-id="ba67e-123">The name of gateway auth key to be regenerated, either 'key1' or 'key2'.</span></span>

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

### <span data-ttu-id="ba67e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba67e-124">-ResourceGroupName</span></span>
<span data-ttu-id="ba67e-125">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="ba67e-125">The resource group name.</span></span>

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

### <span data-ttu-id="ba67e-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ba67e-126">-Confirm</span></span>
<span data-ttu-id="ba67e-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ba67e-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba67e-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba67e-128">-WhatIf</span></span>
<span data-ttu-id="ba67e-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ba67e-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ba67e-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ba67e-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba67e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba67e-131">CommonParameters</span></span>
<span data-ttu-id="ba67e-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ba67e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba67e-133">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba67e-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba67e-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ba67e-134">INPUTS</span></span>

### <span data-ttu-id="ba67e-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="ba67e-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="ba67e-136">System. String</span><span class="sxs-lookup"><span data-stu-id="ba67e-136">System.String</span></span>

## <span data-ttu-id="ba67e-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ba67e-137">OUTPUTS</span></span>

### <span data-ttu-id="ba67e-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGatewayAuthKey</span><span class="sxs-lookup"><span data-stu-id="ba67e-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGatewayAuthKey</span></span>

## <span data-ttu-id="ba67e-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ba67e-139">NOTES</span></span>
* <span data-ttu-id="ba67e-140">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak</span><span class="sxs-lookup"><span data-stu-id="ba67e-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="ba67e-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ba67e-141">RELATED LINKS</span></span>

<span data-ttu-id="ba67e-142">[Új – AzDataFactoryGateway](./New-AzDataFactoryGateway.md) 
 [Get-AzDataFactoryGatewayAuthKey](./Get-AzDataFactoryGatewayAuthKey.md)</span><span class="sxs-lookup"><span data-stu-id="ba67e-142">[New-AzDataFactoryGateway](./New-AzDataFactoryGateway.md)
[Get-AzDataFactoryGatewayAuthKey](./Get-AzDataFactoryGatewayAuthKey.md)</span></span>

