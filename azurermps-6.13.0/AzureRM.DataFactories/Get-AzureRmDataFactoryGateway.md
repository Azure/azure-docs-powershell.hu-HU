---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: D85FF5ED-23EA-48C7-8E61-D931713E0064
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactorygateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryGateway.md
ms.openlocfilehash: 401a72732c59a6dbcdb23c3df1a2f57e5f016315
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502999"
---
# <span data-ttu-id="0456b-101">Get-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="0456b-101">Get-AzureRmDataFactoryGateway</span></span>

## <span data-ttu-id="0456b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0456b-102">SYNOPSIS</span></span>
<span data-ttu-id="0456b-103">Információt kap az Azure Data Factory logikai átjáróról.</span><span class="sxs-lookup"><span data-stu-id="0456b-103">Gets information about logical gateways in Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0456b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0456b-104">SYNTAX</span></span>

### <span data-ttu-id="0456b-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0456b-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryGateway [-DataFactoryName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0456b-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="0456b-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryGateway [-DataFactory] <PSDataFactory> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0456b-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="0456b-107">DESCRIPTION</span></span>
<span data-ttu-id="0456b-108">A **Get-AzureRmDataFactoryGateway** parancsmag az Azure Data Factory logikai átjárókkal kapcsolatos információkat kap.</span><span class="sxs-lookup"><span data-stu-id="0456b-108">The **Get-AzureRmDataFactoryGateway** cmdlet gets information about logical gateways in Azure Data Factory.</span></span>
<span data-ttu-id="0456b-109">Ha az átjáró nevét adja meg, ez a parancsmag információt kap az átjáróról.</span><span class="sxs-lookup"><span data-stu-id="0456b-109">If you specify the name of a gateway, this cmdlet gets information about that gateway.</span></span>
<span data-ttu-id="0456b-110">Ha nem ad meg nevet, ez a parancsmag információkat kap az adatfeldolgozó összes átjáróról.</span><span class="sxs-lookup"><span data-stu-id="0456b-110">If you do not specify a name, this cmdlet gets information about all gateways for a data factory.</span></span>
<span data-ttu-id="0456b-111">Ha helyszíni Microsoft SQL Servert szeretne hozzáadni egy adatfeldolgozóhoz, akkor a helyszíni számítógépre kell telepítenie egy átjárót.</span><span class="sxs-lookup"><span data-stu-id="0456b-111">If you want to add an on-premises Microsoft SQL Server as a linked service to a data factory, you must install a gateway on your on-premises computer.</span></span>

## <span data-ttu-id="0456b-112">Példák</span><span class="sxs-lookup"><span data-stu-id="0456b-112">EXAMPLES</span></span>

### <span data-ttu-id="0456b-113">Példa 1: az összes logikai átjáró beolvasása egy adatgyárban</span><span class="sxs-lookup"><span data-stu-id="0456b-113">Example 1: Get all logical gateways in a data factory</span></span>
```
PS C:\>Get-AzureRmDataFactoryGateway -ResourceGroupName "ADF" -DataFactoryName "WikiADF"
Name            : gateway1
Description     : 
Version         : 1.3.5338.1
Status          : Online
VersionStatus   : UpToDate
CreateTime      : 8/22/2014 1:40:34 AM
RegisterTime    : 8/22/2014 1:41:46 AM
LastConnectTime : 8/22/2014 1:44:56 AM
ExpiryTime      : 
Name            : gateway2
Description     : 
Version         : 1.3.5338.1
Status          : Offline
VersionStatus   : UpToDate
CreateTime      : 8/29/2014 1:46:44 AM
RegisterTime    : 8/29/2014 1:48:36 AM
LastConnectTime : 8/29/2014 1:56:56 AM
ExpiryTime      :
```

<span data-ttu-id="0456b-114">Ez a parancs információkat kap az ADF nevű erőforráscsoport WikiADF nevű adatfeldolgozó összes logikai átjáróról.</span><span class="sxs-lookup"><span data-stu-id="0456b-114">This command gets information about all logical gateways for the data factory named WikiADF in the resource group named ADF.</span></span>

### <span data-ttu-id="0456b-115">2. példa: adott logikai átjáró beszerzése adatgyárban</span><span class="sxs-lookup"><span data-stu-id="0456b-115">Example 2: Get a specific logical gateway in a data factory</span></span>
```
PS C:\>Get-AzureRmDataFactoryGateway -ResourceGroupName "ADF" -Name "Gateway01" -DataFactoryName "WikiADF"
Name            : Gateway01
Description     : 
Version         : 1.3.5338.1
Status          : Online
VersionStatus   : UpToDate
CreateTime      : 8/22/2014 1:40:34 AM
RegisterTime    : 8/22/2014 1:41:46 AM
LastConnectTime : 8/22/2014 1:44:56 AM
ExpiryTime      :
```

<span data-ttu-id="0456b-116">Ez a parancs információt kap az ADF nevű erőforráscsoport WikiADF nevű Gateway01 nevű logikai átjáróról.</span><span class="sxs-lookup"><span data-stu-id="0456b-116">This command gets information about the logical gateway named Gateway01 in the data factory named WikiADF in the resource group named ADF.</span></span>

## <span data-ttu-id="0456b-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0456b-117">PARAMETERS</span></span>

### <span data-ttu-id="0456b-118">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="0456b-118">-DataFactory</span></span>
<span data-ttu-id="0456b-119">Egy **PSDataFactory** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="0456b-119">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="0456b-120">Ez a parancsmag információt ad az adatfeldolgozó logikai átjárókkal kapcsolatban, és ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="0456b-120">This cmdlet gets information about logical gateways in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="0456b-121">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="0456b-121">-DataFactoryName</span></span>
<span data-ttu-id="0456b-122">Az adatfeldolgozó nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0456b-122">Specifies the name of a data factory.</span></span>
<span data-ttu-id="0456b-123">Ez a parancsmag információt ad az adatfeldolgozó logikai átjárókkal kapcsolatban, és ezt a paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="0456b-123">This cmdlet gets information about logical gateways in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="0456b-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0456b-124">-DefaultProfile</span></span>
<span data-ttu-id="0456b-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="0456b-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0456b-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0456b-126">-Name</span></span>
<span data-ttu-id="0456b-127">Annak a logikai átjárónak a neve, amelyről információt szeretne kapni.</span><span class="sxs-lookup"><span data-stu-id="0456b-127">Specifies the name of the logical gateway about which to get information.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0456b-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0456b-128">-ResourceGroupName</span></span>
<span data-ttu-id="0456b-129">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0456b-129">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="0456b-130">Ez a parancsmag olyan logikai átjárók adatait kapja meg, amelyek a paraméter által megadott csoportba tartoznak.</span><span class="sxs-lookup"><span data-stu-id="0456b-130">This cmdlet gets information about logical gateways that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="0456b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0456b-131">CommonParameters</span></span>
<span data-ttu-id="0456b-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0456b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0456b-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0456b-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0456b-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0456b-134">INPUTS</span></span>

### <span data-ttu-id="0456b-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="0456b-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="0456b-136">System. String</span><span class="sxs-lookup"><span data-stu-id="0456b-136">System.String</span></span>

## <span data-ttu-id="0456b-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0456b-137">OUTPUTS</span></span>

### <span data-ttu-id="0456b-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="0456b-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span></span>

## <span data-ttu-id="0456b-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0456b-139">NOTES</span></span>
* <span data-ttu-id="0456b-140">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak</span><span class="sxs-lookup"><span data-stu-id="0456b-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="0456b-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0456b-141">RELATED LINKS</span></span>

[<span data-ttu-id="0456b-142">Új – AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="0456b-142">New-AzureRmDataFactoryGateway</span></span>](./New-AzureRmDataFactoryGateway.md)

[<span data-ttu-id="0456b-143">Remove-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="0456b-143">Remove-AzureRmDataFactoryGateway</span></span>](./Remove-AzureRmDataFactoryGateway.md)

[<span data-ttu-id="0456b-144">Set-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="0456b-144">Set-AzureRmDataFactoryGateway</span></span>](./Set-AzureRmDataFactoryGateway.md)

