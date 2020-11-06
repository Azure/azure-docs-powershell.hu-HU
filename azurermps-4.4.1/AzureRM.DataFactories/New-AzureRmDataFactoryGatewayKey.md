---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 8546C3FE-5396-4027-BF33-F98F6C018A67
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryGatewayKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryGatewayKey.md
ms.openlocfilehash: f1676d385b23711e71fbec5fb5d9131add4daaf4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497099"
---
# <span data-ttu-id="31a19-101">New-AzureRmDataFactoryGatewayKey</span><span class="sxs-lookup"><span data-stu-id="31a19-101">New-AzureRmDataFactoryGatewayKey</span></span>

## <span data-ttu-id="31a19-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="31a19-102">SYNOPSIS</span></span>
<span data-ttu-id="31a19-103">Az Azure Data Factory átjáró kulcsát hozza létre.</span><span class="sxs-lookup"><span data-stu-id="31a19-103">Creates a gateway key for an Azure Data Factory.</span></span> <span data-ttu-id="31a19-104">Ez a parancsmag megszűnt, és Ehelyett használja az **új AzureRmDataFactoryGatewayAuthKey** .</span><span class="sxs-lookup"><span data-stu-id="31a19-104">This cmdlet is deprecated, and you should use **New-AzureRmDataFactoryGatewayAuthKey** instead.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="31a19-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="31a19-105">SYNTAX</span></span>

### <span data-ttu-id="31a19-106">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="31a19-106">ByFactoryName (Default)</span></span>
```
New-AzureRmDataFactoryGatewayKey [-DataFactoryName] <String> [-GatewayName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="31a19-107">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="31a19-107">ByFactoryObject</span></span>
```
New-AzureRmDataFactoryGatewayKey [-DataFactory] <PSDataFactory> [-GatewayName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="31a19-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="31a19-108">DESCRIPTION</span></span>
<span data-ttu-id="31a19-109">A **New-AzureRmDataFactoryGatewayKey** parancsmag létrehoz egy átjáró kulcsot egy megadott Azure Data Factory átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="31a19-109">The **New-AzureRmDataFactoryGatewayKey** cmdlet creates a gateway key for a specified Azure Data Factory gateway.</span></span>
<span data-ttu-id="31a19-110">Ezzel a kulccsal regisztrálja az átjárót egy Felhőbeli szolgáltatással.</span><span class="sxs-lookup"><span data-stu-id="31a19-110">You register the gateway with a cloud service by using this key.</span></span> <span data-ttu-id="31a19-111">Ez a parancsmag megszűnt, és Ehelyett használja az **új AzureRmDataFactoryGatewayAuthKey** .</span><span class="sxs-lookup"><span data-stu-id="31a19-111">This cmdlet is deprecated, and you should use **New-AzureRmDataFactoryGatewayAuthKey** instead.</span></span>

## <span data-ttu-id="31a19-112">Példák</span><span class="sxs-lookup"><span data-stu-id="31a19-112">EXAMPLES</span></span>

### <span data-ttu-id="31a19-113">1. példa: átjáró-kulcs létrehozása</span><span class="sxs-lookup"><span data-stu-id="31a19-113">Example 1: Create a gateway key</span></span>
```
PS C:\>New-AzureRmDataFactoryGatewayKey -ResourceGroupName "ADF" -GatewayName "ContosoGateway" -DataFactoryName "WikiADF" | Format-List
GatewayKey : ADF#40cbb3d9-2736-4794-a8a6-e6b839b4894f@a2d875ce-c9d7-4b8b-ad65-dd3ebbb9a940@8c0d1801-e863-44af-82e6-fb2f0c00f2ae@xz#Y9R0NhAeH3u7wgnrJyiWj4Y/QIhH4fFilIdzZgwsVQA=
```

<span data-ttu-id="31a19-114">Ez a parancs létrehozza az ContosoGateway nevű adatfeldolgozó-átjáró számára az átjáró kulcsát, majd a pipeline operátor segítségével átadja az átjáró kulcsát az Format-List parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="31a19-114">This command creates a gateway key for the data factory gateway named ContosoGateway, and then passes the gateway key to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="31a19-115">További információért írja be a következőt: `Get-Help Format-List` .</span><span class="sxs-lookup"><span data-stu-id="31a19-115">For more information, type `Get-Help Format-List`.</span></span>

## <span data-ttu-id="31a19-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="31a19-116">PARAMETERS</span></span>

### <span data-ttu-id="31a19-117">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="31a19-117">-DataFactory</span></span>
<span data-ttu-id="31a19-118">Egy **PSDataFactory** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="31a19-118">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="31a19-119">Ez a parancsmag létrehoz egy átjáró kulcsot az adatfeldolgozóhoz, amely ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="31a19-119">This cmdlet creates a gateway key for the data factory that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31a19-120">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="31a19-120">-DataFactoryName</span></span>
<span data-ttu-id="31a19-121">Az adatfeldolgozó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="31a19-121">Specifies the name of a data factory.</span></span>
<span data-ttu-id="31a19-122">Ez a parancsmag létrehoz egy átjáró kulcsot az adatfeldolgozóhoz, amely ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="31a19-122">This cmdlet creates a gateway key for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="31a19-123">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="31a19-123">-GatewayName</span></span>
<span data-ttu-id="31a19-124">Az átjáró nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="31a19-124">Specifies the name of the gateway.</span></span>
<span data-ttu-id="31a19-125">Ez a parancsmag létrehoz egy kulcsot a paraméter által megadott átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="31a19-125">This cmdlet creates a key for the gateway that this parameter specifies.</span></span>

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

### <span data-ttu-id="31a19-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31a19-126">-ResourceGroupName</span></span>
<span data-ttu-id="31a19-127">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="31a19-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="31a19-128">Ez a parancsmag létrehoz egy kulcsot egy olyan átjáróhoz, amely a paraméter által definiált csoportba tartozik.</span><span class="sxs-lookup"><span data-stu-id="31a19-128">This cmdlet creates a key for a gateway that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="31a19-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31a19-129">-DefaultProfile</span></span>
<span data-ttu-id="31a19-130">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="31a19-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="31a19-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31a19-131">CommonParameters</span></span>
<span data-ttu-id="31a19-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="31a19-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31a19-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31a19-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31a19-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="31a19-134">INPUTS</span></span>

## <span data-ttu-id="31a19-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="31a19-135">OUTPUTS</span></span>

### <span data-ttu-id="31a19-136">Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryGatewayKey</span><span class="sxs-lookup"><span data-stu-id="31a19-136">Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryGatewayKey</span></span>

## <span data-ttu-id="31a19-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="31a19-137">NOTES</span></span>
* <span data-ttu-id="31a19-138">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak</span><span class="sxs-lookup"><span data-stu-id="31a19-138">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="31a19-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="31a19-139">RELATED LINKS</span></span>

<span data-ttu-id="31a19-140">[Új – AzureRmDataFactoryGateway](./New-AzureRmDataFactoryGateway.md) 
 [Get-AzureRmDataFactoryGatewayAuthKey](./Get-AzureRmDataFactoryGatewayAuthKey.md) 
 [Új – AzureRmDataFactoryGatewayAuthKey](./New-AzureRmDataFactoryGatewayAuthKey.md)</span><span class="sxs-lookup"><span data-stu-id="31a19-140">[New-AzureRmDataFactoryGateway](./New-AzureRmDataFactoryGateway.md)
[Get-AzureRmDataFactoryGatewayAuthKey](./Get-AzureRmDataFactoryGatewayAuthKey.md)
[New-AzureRmDataFactoryGatewayAuthKey](./New-AzureRmDataFactoryGatewayAuthKey.md)</span></span>


