---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactorygatewayauthkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryGatewayAuthKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryGatewayAuthKey.md
ms.openlocfilehash: 8e86597292a9bcfef2163100d273d1e27daeb32a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182533"
---
# <span data-ttu-id="0e560-101">Get-AzDataFactoryGatewayAuthKey</span><span class="sxs-lookup"><span data-stu-id="0e560-101">Get-AzDataFactoryGatewayAuthKey</span></span>

## <span data-ttu-id="0e560-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0e560-102">SYNOPSIS</span></span>
<span data-ttu-id="0e560-103">Az Azure Data Factory átjáró Auth kulcsát kapja.</span><span class="sxs-lookup"><span data-stu-id="0e560-103">Gets gateway auth key for an Azure Data Factory.</span></span>

## <span data-ttu-id="0e560-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0e560-104">SYNTAX</span></span>

### <span data-ttu-id="0e560-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0e560-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryGatewayAuthKey [-DataFactoryName] <String> [-GatewayName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0e560-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="0e560-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryGatewayAuthKey [-InputObject] <PSDataFactory> [-GatewayName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0e560-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="0e560-107">DESCRIPTION</span></span>
<span data-ttu-id="0e560-108">A **Get-AzDataFactoryGatewayAuthKey** parancsmag az Azure Data Factory átjárójának átjáró hitelesítő kulcsát kapja.</span><span class="sxs-lookup"><span data-stu-id="0e560-108">The **Get-AzDataFactoryGatewayAuthKey** cmdlet gets gateway auth key for a specified Azure Data Factory gateway.</span></span>
<span data-ttu-id="0e560-109">Az átjárót egy felhőalapú szolgáltatással regisztrálja az key1 vagy az azonosító2.</span><span class="sxs-lookup"><span data-stu-id="0e560-109">You register the gateway with a cloud service by using this key1 or key2 of this auth key.</span></span>

## <span data-ttu-id="0e560-110">Példák</span><span class="sxs-lookup"><span data-stu-id="0e560-110">EXAMPLES</span></span>

### <span data-ttu-id="0e560-111">Példa 1: átjáró hitelesítő kulcsának beolvasása</span><span class="sxs-lookup"><span data-stu-id="0e560-111">Example 1: Gets auth key of a gateway</span></span>
```
PS C:\> Get-AzDataFactoryGatewayAuthKey -ResourceGroup ADFResource -GatewayName 'MyGateway' -DataFactoryName MyADF
Key1 : DMG@632e739e-1053-4070-9102-8591f067526e@41fcbc45-c594-4152-a8f1-fcbcd6452aea@wu@ZgBjjX6GfJcrzTQInEV9PoOqsDrqOmC
       gGHqUg1THLqA=
Key2 : DMG@632e739e-1053-4070-9102-8591f067526e@41fcbc45-c594-4152-a8f1-fcbcd6452aea@wu@kFXxBdFCEBeL7LPB3hA3LqLd1uNFbyv
       YmWxtV4WD3JQ=
```

<span data-ttu-id="0e560-112">Ez a parancs beolvassa az átjáró hitelesítési kulcsát a MyGateway nevű Data Factory átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="0e560-112">This command gets gateway auth key for the data factory gateway named MyGateway.</span></span>

## <span data-ttu-id="0e560-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0e560-113">PARAMETERS</span></span>

### <span data-ttu-id="0e560-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="0e560-114">-DataFactoryName</span></span>
<span data-ttu-id="0e560-115">Az adatgyári név.</span><span class="sxs-lookup"><span data-stu-id="0e560-115">The data factory name.</span></span>

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

### <span data-ttu-id="0e560-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e560-116">-DefaultProfile</span></span>
<span data-ttu-id="0e560-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="0e560-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0e560-118">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="0e560-118">-GatewayName</span></span>
<span data-ttu-id="0e560-119">Az adatgyári átjáró neve.</span><span class="sxs-lookup"><span data-stu-id="0e560-119">The data factory gateway name.</span></span>

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

### <span data-ttu-id="0e560-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0e560-120">-InputObject</span></span>
<span data-ttu-id="0e560-121">Az Data Factory objektum</span><span class="sxs-lookup"><span data-stu-id="0e560-121">The data factory object</span></span>

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

### <span data-ttu-id="0e560-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e560-122">-ResourceGroupName</span></span>
<span data-ttu-id="0e560-123">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="0e560-123">The resource group name.</span></span>

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

### <span data-ttu-id="0e560-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e560-124">CommonParameters</span></span>
<span data-ttu-id="0e560-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0e560-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e560-126">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e560-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e560-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0e560-127">INPUTS</span></span>

### <span data-ttu-id="0e560-128">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="0e560-128">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="0e560-129">System. String</span><span class="sxs-lookup"><span data-stu-id="0e560-129">System.String</span></span>

## <span data-ttu-id="0e560-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0e560-130">OUTPUTS</span></span>

### <span data-ttu-id="0e560-131">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGatewayAuthKey</span><span class="sxs-lookup"><span data-stu-id="0e560-131">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGatewayAuthKey</span></span>

## <span data-ttu-id="0e560-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0e560-132">NOTES</span></span>
* <span data-ttu-id="0e560-133">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak</span><span class="sxs-lookup"><span data-stu-id="0e560-133">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="0e560-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0e560-134">RELATED LINKS</span></span>

<span data-ttu-id="0e560-135">[Új – AzDataFactoryGateway](./New-AzDataFactoryGateway.md) 
 [Új – AzDataFactoryGatewayAuthKey](./New-AzDataFactoryGatewayAuthKey.md)</span><span class="sxs-lookup"><span data-stu-id="0e560-135">[New-AzDataFactoryGateway](./New-AzDataFactoryGateway.md)
[New-AzDataFactoryGatewayAuthKey](./New-AzDataFactoryGatewayAuthKey.md)</span></span>

