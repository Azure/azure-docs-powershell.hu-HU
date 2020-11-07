---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 4DCF54BA-CFFA-4555-8CA3-66B98F704EFB
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactorygateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryGateway.md
ms.openlocfilehash: a4c755ab3f68eab2821807e7df6b9e24fad0df9d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847230"
---
# <span data-ttu-id="7658f-101">New-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="7658f-101">New-AzDataFactoryGateway</span></span>

## <span data-ttu-id="7658f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7658f-102">SYNOPSIS</span></span>
<span data-ttu-id="7658f-103">Átjárót hoz létre egy Azure Data Factory számára.</span><span class="sxs-lookup"><span data-stu-id="7658f-103">Creates a gateway for an Azure Data Factory.</span></span>

## <span data-ttu-id="7658f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7658f-104">SYNTAX</span></span>

### <span data-ttu-id="7658f-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7658f-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryGateway [-DataFactoryName] <String> [-Name] <String> [[-Description] <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7658f-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="7658f-106">ByFactoryObject</span></span>
```
New-AzDataFactoryGateway [-DataFactory] <PSDataFactory> [-Name] <String> [[-Description] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7658f-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="7658f-107">DESCRIPTION</span></span>
<span data-ttu-id="7658f-108">A **New-AzDataFactoryGateway** parancsmag átjárót hoz létre az Azure Data Factory-ban.</span><span class="sxs-lookup"><span data-stu-id="7658f-108">The **New-AzDataFactoryGateway** cmdlet creates a gateway in Azure Data Factory.</span></span>

## <span data-ttu-id="7658f-109">Példák</span><span class="sxs-lookup"><span data-stu-id="7658f-109">EXAMPLES</span></span>

### <span data-ttu-id="7658f-110">Példa 1: átjáró létrehozása</span><span class="sxs-lookup"><span data-stu-id="7658f-110">Example 1: Create a gateway</span></span>
```
PS C:\>New-AzDataFactoryGateway -ResourceGroupName "ADF" -Name "ContosoGateway" -DataFactoryName "WikiADF" -Description "my gateway"
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

<span data-ttu-id="7658f-111">Ez a parancs létrehoz egy ContosoGateway nevű átjárót az WikiADF nevű adatgyárban az ADF nevű erőforrás csoportban.</span><span class="sxs-lookup"><span data-stu-id="7658f-111">This command creates a gateway named ContosoGateway in the data factory named WikiADF in the resource group named ADF.</span></span>

## <span data-ttu-id="7658f-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7658f-112">PARAMETERS</span></span>

### <span data-ttu-id="7658f-113">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="7658f-113">-DataFactory</span></span>
<span data-ttu-id="7658f-114">Egy **PSDataFactory** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="7658f-114">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="7658f-115">Ez a parancsmag létrehoz egy átjárót az adatfeldolgozó számára, amely ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="7658f-115">This cmdlet creates a gateway for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="7658f-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="7658f-116">-DataFactoryName</span></span>
<span data-ttu-id="7658f-117">Az adatfeldolgozó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7658f-117">Specifies the name of a data factory.</span></span>
<span data-ttu-id="7658f-118">Ez a parancsmag létrehoz egy átjárót az adatfeldolgozó számára, amely ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="7658f-118">This cmdlet creates a gateway for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="7658f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7658f-119">-DefaultProfile</span></span>
<span data-ttu-id="7658f-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="7658f-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7658f-121">-Leírás</span><span class="sxs-lookup"><span data-stu-id="7658f-121">-Description</span></span>
<span data-ttu-id="7658f-122">Az átjáró leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="7658f-122">Specifies a description for the gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7658f-123">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7658f-123">-Name</span></span>
<span data-ttu-id="7658f-124">A létrehozandó átjáró nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7658f-124">Specifies the name of the gateway to create.</span></span>

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

### <span data-ttu-id="7658f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7658f-125">-ResourceGroupName</span></span>
<span data-ttu-id="7658f-126">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7658f-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="7658f-127">Ez a parancsmag létrehoz egy átjárót, amely a paraméter által definiált csoportba tartozik.</span><span class="sxs-lookup"><span data-stu-id="7658f-127">This cmdlet creates a gateway that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="7658f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7658f-128">CommonParameters</span></span>
<span data-ttu-id="7658f-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7658f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7658f-130">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7658f-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7658f-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7658f-131">INPUTS</span></span>

### <span data-ttu-id="7658f-132">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="7658f-132">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="7658f-133">System. String</span><span class="sxs-lookup"><span data-stu-id="7658f-133">System.String</span></span>

## <span data-ttu-id="7658f-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7658f-134">OUTPUTS</span></span>

### <span data-ttu-id="7658f-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="7658f-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span></span>

## <span data-ttu-id="7658f-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7658f-136">NOTES</span></span>
* <span data-ttu-id="7658f-137">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak</span><span class="sxs-lookup"><span data-stu-id="7658f-137">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="7658f-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7658f-138">RELATED LINKS</span></span>

[<span data-ttu-id="7658f-139">Remove-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="7658f-139">Remove-AzDataFactoryGateway</span></span>](./Remove-AzDataFactoryGateway.md)

[<span data-ttu-id="7658f-140">Set-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="7658f-140">Set-AzDataFactoryGateway</span></span>](./Set-AzDataFactoryGateway.md)

