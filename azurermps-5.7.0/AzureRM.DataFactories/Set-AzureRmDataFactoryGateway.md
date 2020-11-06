---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 663D27A3-0B51-48F5-81D0-8DDBC5A3A33C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/set-azurermdatafactorygateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Set-AzureRmDataFactoryGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Set-AzureRmDataFactoryGateway.md
ms.openlocfilehash: 5239f2143eefe40b777ad1077bbd26d6d645754c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493158"
---
# <span data-ttu-id="ae883-101">Set-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="ae883-101">Set-AzureRmDataFactoryGateway</span></span>

## <span data-ttu-id="ae883-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ae883-102">SYNOPSIS</span></span>
<span data-ttu-id="ae883-103">Az Azure Data Factory átjárójának leírását állítja be.</span><span class="sxs-lookup"><span data-stu-id="ae883-103">Sets the description for a gateway in Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ae883-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ae883-104">SYNTAX</span></span>

### <span data-ttu-id="ae883-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ae883-105">ByFactoryName (Default)</span></span>
```
Set-AzureRmDataFactoryGateway [-DataFactoryName] <String> [-Name] <String> [-Description] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ae883-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="ae883-106">ByFactoryObject</span></span>
```
Set-AzureRmDataFactoryGateway [-DataFactory] <PSDataFactory> [-Name] <String> [-Description] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ae883-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="ae883-107">DESCRIPTION</span></span>
<span data-ttu-id="ae883-108">A **set-AzureRmDataFactoryGateway** parancsmag az Azure Data Factory megadott átjárójának leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="ae883-108">The **Set-AzureRmDataFactoryGateway** cmdlet sets the description for the specified gateway in Azure Data Factory.</span></span>

## <span data-ttu-id="ae883-109">Példák</span><span class="sxs-lookup"><span data-stu-id="ae883-109">EXAMPLES</span></span>

### <span data-ttu-id="ae883-110">Példa 1: átjáró leírásának megadása</span><span class="sxs-lookup"><span data-stu-id="ae883-110">Example 1: Set the description for a gateway</span></span>
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

<span data-ttu-id="ae883-111">Ez a parancs a ContosoGateway nevű átjáró leírását állítja be az WikiADF nevű adatgyárban.</span><span class="sxs-lookup"><span data-stu-id="ae883-111">This command sets the description for the gateway named ContosoGateway in the data factory named WikiADF.</span></span>
<span data-ttu-id="ae883-112">A Leírás paraméter az új leírást adja meg.</span><span class="sxs-lookup"><span data-stu-id="ae883-112">The Description parameter specifies the new description.</span></span>

## <span data-ttu-id="ae883-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ae883-113">PARAMETERS</span></span>

### <span data-ttu-id="ae883-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="ae883-114">-DataFactory</span></span>
<span data-ttu-id="ae883-115">Egy **PSDataFactory** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="ae883-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="ae883-116">Ez a parancsmag az adatfeldolgozó átjárójának leírását adja meg, amely ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="ae883-116">This cmdlet sets the description for the gateway in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="ae883-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="ae883-117">-DataFactoryName</span></span>
<span data-ttu-id="ae883-118">Az adatfeldolgozó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ae883-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="ae883-119">Ez a parancsmag az adatfeldolgozó átjárójának leírását adja meg, amely ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="ae883-119">This cmdlet sets the description for the gateway in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="ae883-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae883-120">-DefaultProfile</span></span>
<span data-ttu-id="ae883-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="ae883-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ae883-122">-Leírás</span><span class="sxs-lookup"><span data-stu-id="ae883-122">-Description</span></span>
<span data-ttu-id="ae883-123">Az átjáró leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="ae883-123">Specifies a description for the gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae883-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ae883-124">-Name</span></span>
<span data-ttu-id="ae883-125">Annak az átjárónak a nevét adja meg, amelyhez leírást szeretne megadni.</span><span class="sxs-lookup"><span data-stu-id="ae883-125">Specifies the name of the gateway for which to set a description.</span></span>

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

### <span data-ttu-id="ae883-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae883-126">-ResourceGroupName</span></span>
<span data-ttu-id="ae883-127">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ae883-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="ae883-128">Ez a parancsmag egy olyan átjáró leírását adja meg, amely a paraméter által megadott csoportba tartozik.</span><span class="sxs-lookup"><span data-stu-id="ae883-128">This cmdlet sets the description for a gateway that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="ae883-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae883-129">CommonParameters</span></span>
<span data-ttu-id="ae883-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ae883-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae883-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae883-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae883-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ae883-132">INPUTS</span></span>

### <span data-ttu-id="ae883-133">Nincs</span><span class="sxs-lookup"><span data-stu-id="ae883-133">None</span></span>
<span data-ttu-id="ae883-134">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="ae883-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ae883-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ae883-135">OUTPUTS</span></span>

### <span data-ttu-id="ae883-136">System. Collections. Generic. list ' 1 [[Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryGateway]], Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="ae883-136">System.Collections.Generic.List\`1[[Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryGateway]], Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryGateway</span></span>

## <span data-ttu-id="ae883-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ae883-137">NOTES</span></span>
* <span data-ttu-id="ae883-138">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak</span><span class="sxs-lookup"><span data-stu-id="ae883-138">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="ae883-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ae883-139">RELATED LINKS</span></span>

[<span data-ttu-id="ae883-140">Get-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="ae883-140">Get-AzureRmDataFactoryGateway</span></span>](./Get-AzureRmDataFactoryGateway.md)

[<span data-ttu-id="ae883-141">Új – AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="ae883-141">New-AzureRmDataFactoryGateway</span></span>](./New-AzureRmDataFactoryGateway.md)

[<span data-ttu-id="ae883-142">Remove-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="ae883-142">Remove-AzureRmDataFactoryGateway</span></span>](./Remove-AzureRmDataFactoryGateway.md)


