---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryGatewayAuthKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryGatewayAuthKey.md
ms.openlocfilehash: 9de30d10b34cf666b040c1b25b84e4afeae63a10
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505124"
---
# <span data-ttu-id="e3eb8-101">Get-AzureRmDataFactoryGatewayAuthKey</span><span class="sxs-lookup"><span data-stu-id="e3eb8-101">Get-AzureRmDataFactoryGatewayAuthKey</span></span>

## <span data-ttu-id="e3eb8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e3eb8-102">SYNOPSIS</span></span>
<span data-ttu-id="e3eb8-103">Az Azure Data Factory átjáró Auth kulcsát kapja.</span><span class="sxs-lookup"><span data-stu-id="e3eb8-103">Gets gateway auth key for an Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e3eb8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e3eb8-104">SYNTAX</span></span>

### <span data-ttu-id="e3eb8-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e3eb8-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryGatewayAuthKey [-DataFactoryName] <String> [-GatewayName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e3eb8-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="e3eb8-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryGatewayAuthKey -InputObject <PSDataFactory> [-GatewayName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e3eb8-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="e3eb8-107">DESCRIPTION</span></span>
<span data-ttu-id="e3eb8-108">A **Get-AzureRmDataFactoryGatewayAuthKey** parancsmag az Azure Data Factory átjárójának átjáró hitelesítő kulcsát kapja.</span><span class="sxs-lookup"><span data-stu-id="e3eb8-108">The **Get-AzureRmDataFactoryGatewayAuthKey** cmdlet gets gateway auth key for a specified Azure Data Factory gateway.</span></span>
<span data-ttu-id="e3eb8-109">Az átjárót egy felhőalapú szolgáltatással regisztrálja az key1 vagy az azonosító2.</span><span class="sxs-lookup"><span data-stu-id="e3eb8-109">You register the gateway with a cloud service by using this key1 or key2 of this auth key.</span></span>

## <span data-ttu-id="e3eb8-110">Példák</span><span class="sxs-lookup"><span data-stu-id="e3eb8-110">EXAMPLES</span></span>

### <span data-ttu-id="e3eb8-111">Példa 1: átjáró hitelesítő kulcsának beolvasása</span><span class="sxs-lookup"><span data-stu-id="e3eb8-111">Example 1: Gets auth key of a gateway</span></span>
```
PS C:\> Get-AzureRmDataFactoryGatewayAuthKey -ResourceGroup ADFResource -GatewayName 'MyGateway' -DataFactoryName MyADF
Key1 : DMG@632e739e-1053-4070-9102-8591f067526e@41fcbc45-c594-4152-a8f1-fcbcd6452aea@wu@ZgBjjX6GfJcrzTQInEV9PoOqsDrqOmC
       gGHqUg1THLqA=
Key2 : DMG@632e739e-1053-4070-9102-8591f067526e@41fcbc45-c594-4152-a8f1-fcbcd6452aea@wu@kFXxBdFCEBeL7LPB3hA3LqLd1uNFbyv
       YmWxtV4WD3JQ=
```

<span data-ttu-id="e3eb8-112">Ez a parancs beolvassa az átjáró hitelesítési kulcsát a MyGateway nevű Data Factory átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="e3eb8-112">This command gets gateway auth key for the data factory gateway named MyGateway.</span></span>

## <span data-ttu-id="e3eb8-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e3eb8-113">PARAMETERS</span></span>

### <span data-ttu-id="e3eb8-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="e3eb8-114">-DataFactoryName</span></span>
<span data-ttu-id="e3eb8-115">Az adatgyári név.</span><span class="sxs-lookup"><span data-stu-id="e3eb8-115">The data factory name.</span></span>

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

### <span data-ttu-id="e3eb8-116">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="e3eb8-116">-GatewayName</span></span>
<span data-ttu-id="e3eb8-117">Az adatgyári átjáró neve.</span><span class="sxs-lookup"><span data-stu-id="e3eb8-117">The data factory gateway name.</span></span>

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

### <span data-ttu-id="e3eb8-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3eb8-118">-ResourceGroupName</span></span>
<span data-ttu-id="e3eb8-119">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="e3eb8-119">The resource group name.</span></span>

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

### <span data-ttu-id="e3eb8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3eb8-120">-DefaultProfile</span></span>
<span data-ttu-id="e3eb8-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e3eb8-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e3eb8-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e3eb8-122">-InputObject</span></span>
<span data-ttu-id="e3eb8-123">Az Data Factory objektum.</span><span class="sxs-lookup"><span data-stu-id="e3eb8-123">The data factory object.</span></span>

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

### <span data-ttu-id="e3eb8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3eb8-124">CommonParameters</span></span>
<span data-ttu-id="e3eb8-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e3eb8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3eb8-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3eb8-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3eb8-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e3eb8-127">INPUTS</span></span>

### <span data-ttu-id="e3eb8-128">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="e3eb8-128">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>
<span data-ttu-id="e3eb8-129">System. String</span><span class="sxs-lookup"><span data-stu-id="e3eb8-129">System.String</span></span>

## <span data-ttu-id="e3eb8-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e3eb8-130">OUTPUTS</span></span>

### <span data-ttu-id="e3eb8-131">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGatewayAuthKey</span><span class="sxs-lookup"><span data-stu-id="e3eb8-131">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGatewayAuthKey</span></span>

## <span data-ttu-id="e3eb8-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e3eb8-132">NOTES</span></span>
* <span data-ttu-id="e3eb8-133">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak</span><span class="sxs-lookup"><span data-stu-id="e3eb8-133">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="e3eb8-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e3eb8-134">RELATED LINKS</span></span>

<span data-ttu-id="e3eb8-135">[Új – AzureRmDataFactoryGateway](./New-AzureRmDataFactoryGateway.md) 
 [Új – AzureRmDataFactoryGatewayAuthKey](./New-AzureRmDataFactoryGatewayAuthKey.md)</span><span class="sxs-lookup"><span data-stu-id="e3eb8-135">[New-AzureRmDataFactoryGateway](./New-AzureRmDataFactoryGateway.md)
[New-AzureRmDataFactoryGatewayAuthKey](./New-AzureRmDataFactoryGatewayAuthKey.md)</span></span>

