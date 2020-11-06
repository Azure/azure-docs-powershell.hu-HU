---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 663D27A3-0B51-48F5-81D0-8DDBC5A3A33C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/set-azurermdatafactorygateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Set-AzureRmDataFactoryGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Set-AzureRmDataFactoryGateway.md
ms.openlocfilehash: c40999dfa9f1300502e8909a32eaf13a34d0bae0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499635"
---
# <span data-ttu-id="bdcf2-101">Set-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="bdcf2-101">Set-AzureRmDataFactoryGateway</span></span>

## <span data-ttu-id="bdcf2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bdcf2-102">SYNOPSIS</span></span>
<span data-ttu-id="bdcf2-103">Az Azure Data Factory átjárójának leírását állítja be.</span><span class="sxs-lookup"><span data-stu-id="bdcf2-103">Sets the description for a gateway in Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bdcf2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bdcf2-104">SYNTAX</span></span>

### <span data-ttu-id="bdcf2-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="bdcf2-105">ByFactoryName (Default)</span></span>
```
Set-AzureRmDataFactoryGateway [-DataFactoryName] <String> [-Name] <String> [-Description] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bdcf2-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="bdcf2-106">ByFactoryObject</span></span>
```
Set-AzureRmDataFactoryGateway [-DataFactory] <PSDataFactory> [-Name] <String> [-Description] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bdcf2-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="bdcf2-107">DESCRIPTION</span></span>
<span data-ttu-id="bdcf2-108">A **set-AzureRmDataFactoryGateway** parancsmag az Azure Data Factory megadott átjárójának leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="bdcf2-108">The **Set-AzureRmDataFactoryGateway** cmdlet sets the description for the specified gateway in Azure Data Factory.</span></span>

## <span data-ttu-id="bdcf2-109">Példák</span><span class="sxs-lookup"><span data-stu-id="bdcf2-109">EXAMPLES</span></span>

### <span data-ttu-id="bdcf2-110">Példa 1: átjáró leírásának megadása</span><span class="sxs-lookup"><span data-stu-id="bdcf2-110">Example 1: Set the description for a gateway</span></span>
```
PS C:\>Set-AzureRmDataFactoryGateway -ResourceGroupName "ADF" -Name "ContosoGateway" -DataFactoryName "WikiADF" -Description "my gateway"
Name            : ContosoGateway
Description     : my gateway
Version         : 1.3.5338.1
Status          : Online
VersionStatus   : UpToDate
CreateTime      : 8/22/2014 1:31:09 AM
RegisterTime    : 8/22/2014 1:31:37 AM
LastConnectTime : 8/22/2014 1:41:41 AM
ExpiryTime      :
```

<span data-ttu-id="bdcf2-111">Ez a parancs a ContosoGateway nevű átjáró leírását állítja be az WikiADF nevű adatgyárban.</span><span class="sxs-lookup"><span data-stu-id="bdcf2-111">This command sets the description for the gateway named ContosoGateway in the data factory named WikiADF.</span></span>
<span data-ttu-id="bdcf2-112">A Leírás paraméter az új leírást adja meg.</span><span class="sxs-lookup"><span data-stu-id="bdcf2-112">The Description parameter specifies the new description.</span></span>

## <span data-ttu-id="bdcf2-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bdcf2-113">PARAMETERS</span></span>

### <span data-ttu-id="bdcf2-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="bdcf2-114">-DataFactory</span></span>
<span data-ttu-id="bdcf2-115">Egy **PSDataFactory** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="bdcf2-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="bdcf2-116">Ez a parancsmag az adatfeldolgozó átjárójának leírását adja meg, amely ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="bdcf2-116">This cmdlet sets the description for the gateway in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="bdcf2-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="bdcf2-117">-DataFactoryName</span></span>
<span data-ttu-id="bdcf2-118">Az adatfeldolgozó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bdcf2-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="bdcf2-119">Ez a parancsmag az adatfeldolgozó átjárójának leírását adja meg, amely ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="bdcf2-119">This cmdlet sets the description for the gateway in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="bdcf2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdcf2-120">-DefaultProfile</span></span>
<span data-ttu-id="bdcf2-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="bdcf2-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bdcf2-122">-Leírás</span><span class="sxs-lookup"><span data-stu-id="bdcf2-122">-Description</span></span>
<span data-ttu-id="bdcf2-123">Az átjáró leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="bdcf2-123">Specifies a description for the gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdcf2-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="bdcf2-124">-Name</span></span>
<span data-ttu-id="bdcf2-125">Annak az átjárónak a nevét adja meg, amelyhez leírást szeretne megadni.</span><span class="sxs-lookup"><span data-stu-id="bdcf2-125">Specifies the name of the gateway for which to set a description.</span></span>

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

### <span data-ttu-id="bdcf2-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bdcf2-126">-ResourceGroupName</span></span>
<span data-ttu-id="bdcf2-127">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bdcf2-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="bdcf2-128">Ez a parancsmag egy olyan átjáró leírását adja meg, amely a paraméter által megadott csoportba tartozik.</span><span class="sxs-lookup"><span data-stu-id="bdcf2-128">This cmdlet sets the description for a gateway that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="bdcf2-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdcf2-129">CommonParameters</span></span>
<span data-ttu-id="bdcf2-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bdcf2-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdcf2-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bdcf2-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdcf2-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bdcf2-132">INPUTS</span></span>

### <span data-ttu-id="bdcf2-133">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="bdcf2-133">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="bdcf2-134">System. String</span><span class="sxs-lookup"><span data-stu-id="bdcf2-134">System.String</span></span>

## <span data-ttu-id="bdcf2-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bdcf2-135">OUTPUTS</span></span>

### <span data-ttu-id="bdcf2-136">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="bdcf2-136">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span></span>

## <span data-ttu-id="bdcf2-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bdcf2-137">NOTES</span></span>
* <span data-ttu-id="bdcf2-138">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak</span><span class="sxs-lookup"><span data-stu-id="bdcf2-138">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="bdcf2-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bdcf2-139">RELATED LINKS</span></span>

[<span data-ttu-id="bdcf2-140">Get-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="bdcf2-140">Get-AzureRmDataFactoryGateway</span></span>](./Get-AzureRmDataFactoryGateway.md)

[<span data-ttu-id="bdcf2-141">Új – AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="bdcf2-141">New-AzureRmDataFactoryGateway</span></span>](./New-AzureRmDataFactoryGateway.md)

[<span data-ttu-id="bdcf2-142">Remove-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="bdcf2-142">Remove-AzureRmDataFactoryGateway</span></span>](./Remove-AzureRmDataFactoryGateway.md)


