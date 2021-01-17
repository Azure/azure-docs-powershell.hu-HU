---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactorygatewayauthkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryGatewayAuthKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryGatewayAuthKey.md
ms.openlocfilehash: 8e86597292a9bcfef2163100d273d1e27daeb32a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480444"
---
# <span data-ttu-id="43201-101">Get-AzDataFactoryGatewayAuthKey</span><span class="sxs-lookup"><span data-stu-id="43201-101">Get-AzDataFactoryGatewayAuthKey</span></span>

## <span data-ttu-id="43201-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43201-102">SYNOPSIS</span></span>
<span data-ttu-id="43201-103">Átjáró-hitelesítési kulcsot kap egy Azure Data Factoryhoz.</span><span class="sxs-lookup"><span data-stu-id="43201-103">Gets gateway auth key for an Azure Data Factory.</span></span>

## <span data-ttu-id="43201-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="43201-104">SYNTAX</span></span>

### <span data-ttu-id="43201-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="43201-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryGatewayAuthKey [-DataFactoryName] <String> [-GatewayName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="43201-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="43201-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryGatewayAuthKey [-InputObject] <PSDataFactory> [-GatewayName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="43201-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="43201-107">DESCRIPTION</span></span>
<span data-ttu-id="43201-108">A **Get-AzDataFactoryGatewayAuthKey** parancsmag átjárókulcsot kap egy megadott Azure Data Factory-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="43201-108">The **Get-AzDataFactoryGatewayAuthKey** cmdlet gets gateway auth key for a specified Azure Data Factory gateway.</span></span>
<span data-ttu-id="43201-109">Ezzel a hitelesítési kulcssal regisztrálhatja az átjárót egy felhőszolgáltatással.</span><span class="sxs-lookup"><span data-stu-id="43201-109">You register the gateway with a cloud service by using this key1 or key2 of this auth key.</span></span>

## <span data-ttu-id="43201-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="43201-110">EXAMPLES</span></span>

### <span data-ttu-id="43201-111">1. példa: Átjáró hitelesítési kulcsának lekérte</span><span class="sxs-lookup"><span data-stu-id="43201-111">Example 1: Gets auth key of a gateway</span></span>
```
PS C:\> Get-AzDataFactoryGatewayAuthKey -ResourceGroup ADFResource -GatewayName 'MyGateway' -DataFactoryName MyADF
Key1 : DMG@632e739e-1053-4070-9102-8591f067526e@41fcbc45-c594-4152-a8f1-fcbcd6452aea@wu@ZgBjjX6GfJcrzTQInEV9PoOqsDrqOmC
       gGHqUg1THLqA=
Key2 : DMG@632e739e-1053-4070-9102-8591f067526e@41fcbc45-c594-4152-a8f1-fcbcd6452aea@wu@kFXxBdFCEBeL7LPB3hA3LqLd1uNFbyv
       YmWxtV4WD3JQ=
```

<span data-ttu-id="43201-112">Ez a parancs átjáró-hitelesítési kulcsot kap a MyGateway nevű adat gyári átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="43201-112">This command gets gateway auth key for the data factory gateway named MyGateway.</span></span>

## <span data-ttu-id="43201-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="43201-113">PARAMETERS</span></span>

### <span data-ttu-id="43201-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="43201-114">-DataFactoryName</span></span>
<span data-ttu-id="43201-115">Az adatüzem neve.</span><span class="sxs-lookup"><span data-stu-id="43201-115">The data factory name.</span></span>

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

### <span data-ttu-id="43201-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43201-116">-DefaultProfile</span></span>
<span data-ttu-id="43201-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="43201-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="43201-118">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="43201-118">-GatewayName</span></span>
<span data-ttu-id="43201-119">Az adatüzemi átjáró neve.</span><span class="sxs-lookup"><span data-stu-id="43201-119">The data factory gateway name.</span></span>

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

### <span data-ttu-id="43201-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="43201-120">-InputObject</span></span>
<span data-ttu-id="43201-121">The data factory object</span><span class="sxs-lookup"><span data-stu-id="43201-121">The data factory object</span></span>

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

### <span data-ttu-id="43201-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43201-122">-ResourceGroupName</span></span>
<span data-ttu-id="43201-123">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="43201-123">The resource group name.</span></span>

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

### <span data-ttu-id="43201-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43201-124">CommonParameters</span></span>
<span data-ttu-id="43201-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43201-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43201-126">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43201-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43201-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="43201-127">INPUTS</span></span>

### <span data-ttu-id="43201-128">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="43201-128">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="43201-129">System.String</span><span class="sxs-lookup"><span data-stu-id="43201-129">System.String</span></span>

## <span data-ttu-id="43201-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="43201-130">OUTPUTS</span></span>

### <span data-ttu-id="43201-131">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGatewayAuthKey</span><span class="sxs-lookup"><span data-stu-id="43201-131">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGatewayAuthKey</span></span>

## <span data-ttu-id="43201-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="43201-132">NOTES</span></span>
* <span data-ttu-id="43201-133">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, adatok, faktorok</span><span class="sxs-lookup"><span data-stu-id="43201-133">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="43201-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="43201-134">RELATED LINKS</span></span>

<span data-ttu-id="43201-135">[New-AzDataFactoryGateway](./New-AzDataFactoryGateway.md) 
 [New-AzDataFactoryGatewayAuthKey](./New-AzDataFactoryGatewayAuthKey.md)</span><span class="sxs-lookup"><span data-stu-id="43201-135">[New-AzDataFactoryGateway](./New-AzDataFactoryGateway.md)
[New-AzDataFactoryGatewayAuthKey](./New-AzDataFactoryGatewayAuthKey.md)</span></span>

