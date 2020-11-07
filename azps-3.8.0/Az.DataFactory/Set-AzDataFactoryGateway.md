---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 663D27A3-0B51-48F5-81D0-8DDBC5A3A33C
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactorygateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryGateway.md
ms.openlocfilehash: b9eebe26e64e9a7ce2497cdf9984ca6dabb062e0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847150"
---
# <span data-ttu-id="d68e0-101">Set-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="d68e0-101">Set-AzDataFactoryGateway</span></span>

## <span data-ttu-id="d68e0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d68e0-102">SYNOPSIS</span></span>
<span data-ttu-id="d68e0-103">Az Azure Data Factory átjárójának leírását állítja be.</span><span class="sxs-lookup"><span data-stu-id="d68e0-103">Sets the description for a gateway in Azure Data Factory.</span></span>

## <span data-ttu-id="d68e0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d68e0-104">SYNTAX</span></span>

### <span data-ttu-id="d68e0-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d68e0-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryGateway [-DataFactoryName] <String> [-Name] <String> [-Description] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d68e0-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="d68e0-106">ByFactoryObject</span></span>
```
Set-AzDataFactoryGateway [-DataFactory] <PSDataFactory> [-Name] <String> [-Description] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d68e0-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="d68e0-107">DESCRIPTION</span></span>
<span data-ttu-id="d68e0-108">A **set-AzDataFactoryGateway** parancsmag az Azure Data Factory megadott átjárójának leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="d68e0-108">The **Set-AzDataFactoryGateway** cmdlet sets the description for the specified gateway in Azure Data Factory.</span></span>

## <span data-ttu-id="d68e0-109">Példák</span><span class="sxs-lookup"><span data-stu-id="d68e0-109">EXAMPLES</span></span>

### <span data-ttu-id="d68e0-110">Példa 1: átjáró leírásának megadása</span><span class="sxs-lookup"><span data-stu-id="d68e0-110">Example 1: Set the description for a gateway</span></span>
```
PS C:\>Set-AzDataFactoryGateway -ResourceGroupName "ADF" -Name "ContosoGateway" -DataFactoryName "WikiADF" -Description "my gateway"
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

<span data-ttu-id="d68e0-111">Ez a parancs a ContosoGateway nevű átjáró leírását állítja be az WikiADF nevű adatgyárban.</span><span class="sxs-lookup"><span data-stu-id="d68e0-111">This command sets the description for the gateway named ContosoGateway in the data factory named WikiADF.</span></span>
<span data-ttu-id="d68e0-112">A Leírás paraméter az új leírást adja meg.</span><span class="sxs-lookup"><span data-stu-id="d68e0-112">The Description parameter specifies the new description.</span></span>

## <span data-ttu-id="d68e0-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d68e0-113">PARAMETERS</span></span>

### <span data-ttu-id="d68e0-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="d68e0-114">-DataFactory</span></span>
<span data-ttu-id="d68e0-115">Egy **PSDataFactory** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="d68e0-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="d68e0-116">Ez a parancsmag az adatfeldolgozó átjárójának leírását adja meg, amely ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="d68e0-116">This cmdlet sets the description for the gateway in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="d68e0-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="d68e0-117">-DataFactoryName</span></span>
<span data-ttu-id="d68e0-118">Az adatfeldolgozó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d68e0-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="d68e0-119">Ez a parancsmag az adatfeldolgozó átjárójának leírását adja meg, amely ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="d68e0-119">This cmdlet sets the description for the gateway in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="d68e0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d68e0-120">-DefaultProfile</span></span>
<span data-ttu-id="d68e0-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="d68e0-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d68e0-122">-Leírás</span><span class="sxs-lookup"><span data-stu-id="d68e0-122">-Description</span></span>
<span data-ttu-id="d68e0-123">Az átjáró leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="d68e0-123">Specifies a description for the gateway.</span></span>

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

### <span data-ttu-id="d68e0-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d68e0-124">-Name</span></span>
<span data-ttu-id="d68e0-125">Annak az átjárónak a nevét adja meg, amelyhez leírást szeretne megadni.</span><span class="sxs-lookup"><span data-stu-id="d68e0-125">Specifies the name of the gateway for which to set a description.</span></span>

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

### <span data-ttu-id="d68e0-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d68e0-126">-ResourceGroupName</span></span>
<span data-ttu-id="d68e0-127">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d68e0-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="d68e0-128">Ez a parancsmag egy olyan átjáró leírását adja meg, amely a paraméter által megadott csoportba tartozik.</span><span class="sxs-lookup"><span data-stu-id="d68e0-128">This cmdlet sets the description for a gateway that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="d68e0-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d68e0-129">CommonParameters</span></span>
<span data-ttu-id="d68e0-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d68e0-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d68e0-131">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d68e0-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d68e0-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d68e0-132">INPUTS</span></span>

### <span data-ttu-id="d68e0-133">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="d68e0-133">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="d68e0-134">System. String</span><span class="sxs-lookup"><span data-stu-id="d68e0-134">System.String</span></span>

## <span data-ttu-id="d68e0-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d68e0-135">OUTPUTS</span></span>

### <span data-ttu-id="d68e0-136">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="d68e0-136">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span></span>

## <span data-ttu-id="d68e0-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d68e0-137">NOTES</span></span>
* <span data-ttu-id="d68e0-138">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak</span><span class="sxs-lookup"><span data-stu-id="d68e0-138">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="d68e0-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d68e0-139">RELATED LINKS</span></span>

[<span data-ttu-id="d68e0-140">Get-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="d68e0-140">Get-AzDataFactoryGateway</span></span>](./Get-AzDataFactoryGateway.md)

[<span data-ttu-id="d68e0-141">Új – AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="d68e0-141">New-AzDataFactoryGateway</span></span>](./New-AzDataFactoryGateway.md)

[<span data-ttu-id="d68e0-142">Remove-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="d68e0-142">Remove-AzDataFactoryGateway</span></span>](./Remove-AzDataFactoryGateway.md)

