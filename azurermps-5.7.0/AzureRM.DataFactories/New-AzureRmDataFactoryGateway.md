---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 4DCF54BA-CFFA-4555-8CA3-66B98F704EFB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/new-azurermdatafactorygateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryGateway.md
ms.openlocfilehash: 4b94c3e0d178748169b5faaa3b7eb43b76f8bc4c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497652"
---
# <span data-ttu-id="9009a-101">New-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="9009a-101">New-AzureRmDataFactoryGateway</span></span>

## <span data-ttu-id="9009a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9009a-102">SYNOPSIS</span></span>
<span data-ttu-id="9009a-103">Átjárót hoz létre egy Azure Data Factory számára.</span><span class="sxs-lookup"><span data-stu-id="9009a-103">Creates a gateway for an Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9009a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9009a-104">SYNTAX</span></span>

### <span data-ttu-id="9009a-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9009a-105">ByFactoryName (Default)</span></span>
```
New-AzureRmDataFactoryGateway [-DataFactoryName] <String> [-Name] <String> [[-Description] <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9009a-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="9009a-106">ByFactoryObject</span></span>
```
New-AzureRmDataFactoryGateway [-DataFactory] <PSDataFactory> [-Name] <String> [[-Description] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9009a-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="9009a-107">DESCRIPTION</span></span>
<span data-ttu-id="9009a-108">A **New-AzureRmDataFactoryGateway** parancsmag átjárót hoz létre az Azure Data Factory-ban.</span><span class="sxs-lookup"><span data-stu-id="9009a-108">The **New-AzureRmDataFactoryGateway** cmdlet creates a gateway in Azure Data Factory.</span></span>

## <span data-ttu-id="9009a-109">Példák</span><span class="sxs-lookup"><span data-stu-id="9009a-109">EXAMPLES</span></span>

### <span data-ttu-id="9009a-110">Példa 1: átjáró létrehozása</span><span class="sxs-lookup"><span data-stu-id="9009a-110">Example 1: Create a gateway</span></span>
```
PS C:\>New-AzureRmDataFactoryGateway -ResourceGroupName "ADF" -Name "ContosoGateway" -DataFactoryName "WikiADF" -Description "my gateway"
Name              : ContosoGateway
Description       : my gateway
Version           : 
Status            : NeedRegistration
VersionStatus     : None
CreateTime        : 8/22/2014 1:40:34 AM
RegisterTime      : 
LastConnectTime   : 
ExpiryTime        : 
ProvisioningState : Succeeded
Key               : ADF#40cbb3d9-2736-4794-a8a6-e6b839b4894f@a2d875ce-c9d7-4b8b-ad65-dd3ebbb9a940@8c0d1801-e863-44af-82e6-fb2f0c00f2ae@xz#Y9R0NhAeH3u7wgnrJyiWj4Y/QIhH4fFilIdzZgwsVQA=
```

<span data-ttu-id="9009a-111">Ez a parancs létrehoz egy ContosoGateway nevű átjárót az WikiADF nevű adatgyárban az ADF nevű erőforrás csoportban.</span><span class="sxs-lookup"><span data-stu-id="9009a-111">This command creates a gateway named ContosoGateway in the data factory named WikiADF in the resource group named ADF.</span></span>

## <span data-ttu-id="9009a-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9009a-112">PARAMETERS</span></span>

### <span data-ttu-id="9009a-113">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="9009a-113">-DataFactory</span></span>
<span data-ttu-id="9009a-114">Egy **PSDataFactory** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="9009a-114">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="9009a-115">Ez a parancsmag létrehoz egy átjárót az adatfeldolgozó számára, amely ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="9009a-115">This cmdlet creates a gateway for the data factory that this parameter specifies.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9009a-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="9009a-116">-DataFactoryName</span></span>
<span data-ttu-id="9009a-117">Az adatfeldolgozó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9009a-117">Specifies the name of a data factory.</span></span>
<span data-ttu-id="9009a-118">Ez a parancsmag létrehoz egy átjárót az adatfeldolgozó számára, amely ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="9009a-118">This cmdlet creates a gateway for the data factory that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9009a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9009a-119">-DefaultProfile</span></span>
<span data-ttu-id="9009a-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="9009a-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9009a-121">-Leírás</span><span class="sxs-lookup"><span data-stu-id="9009a-121">-Description</span></span>
<span data-ttu-id="9009a-122">Az átjáró leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="9009a-122">Specifies a description for the gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9009a-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9009a-123">-Name</span></span>
<span data-ttu-id="9009a-124">A létrehozandó átjáró nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9009a-124">Specifies the name of the gateway to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9009a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9009a-125">-ResourceGroupName</span></span>
<span data-ttu-id="9009a-126">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9009a-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="9009a-127">Ez a parancsmag létrehoz egy átjárót, amely a paraméter által definiált csoportba tartozik.</span><span class="sxs-lookup"><span data-stu-id="9009a-127">This cmdlet creates a gateway that belongs to the group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9009a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9009a-128">CommonParameters</span></span>
<span data-ttu-id="9009a-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9009a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9009a-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9009a-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9009a-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9009a-131">INPUTS</span></span>

### <span data-ttu-id="9009a-132">Nincs</span><span class="sxs-lookup"><span data-stu-id="9009a-132">None</span></span>
<span data-ttu-id="9009a-133">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="9009a-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9009a-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9009a-134">OUTPUTS</span></span>

### <span data-ttu-id="9009a-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="9009a-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span></span>

## <span data-ttu-id="9009a-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9009a-136">NOTES</span></span>
* <span data-ttu-id="9009a-137">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak</span><span class="sxs-lookup"><span data-stu-id="9009a-137">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="9009a-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9009a-138">RELATED LINKS</span></span>

[<span data-ttu-id="9009a-139">Remove-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="9009a-139">Remove-AzureRmDataFactoryGateway</span></span>](./Remove-AzureRmDataFactoryGateway.md)

[<span data-ttu-id="9009a-140">Set-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="9009a-140">Set-AzureRmDataFactoryGateway</span></span>](./Set-AzureRmDataFactoryGateway.md)


