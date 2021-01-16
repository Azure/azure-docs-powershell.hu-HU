---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: D85FF5ED-23EA-48C7-8E61-D931713E0064
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactorygateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryGateway.md
ms.openlocfilehash: 6d7b82a3046b56b473140b6830a0b04333cba9b0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98354582"
---
# <span data-ttu-id="6a658-101">Get-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="6a658-101">Get-AzDataFactoryGateway</span></span>

## <span data-ttu-id="6a658-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a658-102">SYNOPSIS</span></span>
<span data-ttu-id="6a658-103">Információkat kap az Azure Data Factory logikai átjáróiról.</span><span class="sxs-lookup"><span data-stu-id="6a658-103">Gets information about logical gateways in Azure Data Factory.</span></span>

## <span data-ttu-id="6a658-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6a658-104">SYNTAX</span></span>

### <span data-ttu-id="6a658-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6a658-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryGateway [-DataFactoryName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6a658-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="6a658-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryGateway [-DataFactory] <PSDataFactory> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6a658-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6a658-107">DESCRIPTION</span></span>
<span data-ttu-id="6a658-108">A **Get-AzDataFactoryGateway** parancsmag információt kap az Azure Data Factory logikai átjáróiról.</span><span class="sxs-lookup"><span data-stu-id="6a658-108">The **Get-AzDataFactoryGateway** cmdlet gets information about logical gateways in Azure Data Factory.</span></span>
<span data-ttu-id="6a658-109">Ha megadja egy átjáró nevét, ez a parancsmag információt kap az átjáróról.</span><span class="sxs-lookup"><span data-stu-id="6a658-109">If you specify the name of a gateway, this cmdlet gets information about that gateway.</span></span>
<span data-ttu-id="6a658-110">Ha nem ad meg nevet, ez a parancsmag információt kap egy adatüzem minden átjáróról.</span><span class="sxs-lookup"><span data-stu-id="6a658-110">If you do not specify a name, this cmdlet gets information about all gateways for a data factory.</span></span>
<span data-ttu-id="6a658-111">Ha egy helyszíni Microsoft SQL Servert csatolt szolgáltatásként szeretne hozzáadni egy adatüzemhez, telepítenie kell egy átjárót a helyszíni számítógépén.</span><span class="sxs-lookup"><span data-stu-id="6a658-111">If you want to add an on-premises Microsoft SQL Server as a linked service to a data factory, you must install a gateway on your on-premises computer.</span></span>

## <span data-ttu-id="6a658-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6a658-112">EXAMPLES</span></span>

### <span data-ttu-id="6a658-113">1. példa: Logikai átjárók be szereznie egy adatüzemben</span><span class="sxs-lookup"><span data-stu-id="6a658-113">Example 1: Get all logical gateways in a data factory</span></span>
```
PS C:\>Get-AzDataFactoryGateway -ResourceGroupName "ADF" -DataFactoryName "WikiADF"
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

<span data-ttu-id="6a658-114">Ez a parancs információkat kap az ADF nevű erőforráscsoport WikiADF nevű adatkezelő üzemének összes logikai átjárójára.</span><span class="sxs-lookup"><span data-stu-id="6a658-114">This command gets information about all logical gateways for the data factory named WikiADF in the resource group named ADF.</span></span>

### <span data-ttu-id="6a658-115">2. példa: Konkrét logikai átjáró lekérte egy adatüzemben</span><span class="sxs-lookup"><span data-stu-id="6a658-115">Example 2: Get a specific logical gateway in a data factory</span></span>
```
PS C:\>Get-AzDataFactoryGateway -ResourceGroupName "ADF" -Name "Gateway01" -DataFactoryName "WikiADF"
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

<span data-ttu-id="6a658-116">Ez a parancs információkat kap az ADF nevű erőforráscsoport WikiADF nevű adatüzemében található Átjáró01 nevű logikai átjáróról.</span><span class="sxs-lookup"><span data-stu-id="6a658-116">This command gets information about the logical gateway named Gateway01 in the data factory named WikiADF in the resource group named ADF.</span></span>

## <span data-ttu-id="6a658-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6a658-117">PARAMETERS</span></span>

### <span data-ttu-id="6a658-118">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="6a658-118">-DataFactory</span></span>
<span data-ttu-id="6a658-119">EGY **PSDataFactory-objektumot** ad meg.</span><span class="sxs-lookup"><span data-stu-id="6a658-119">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="6a658-120">Ez a parancsmag információt kap a paraméter által megadott adatüzemi logikai átjárókról.</span><span class="sxs-lookup"><span data-stu-id="6a658-120">This cmdlet gets information about logical gateways in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="6a658-121">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="6a658-121">-DataFactoryName</span></span>
<span data-ttu-id="6a658-122">Egy adatüzem nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6a658-122">Specifies the name of a data factory.</span></span>
<span data-ttu-id="6a658-123">Ez a parancsmag információt kap a paraméter által megadott adatüzemi logikai átjárókról.</span><span class="sxs-lookup"><span data-stu-id="6a658-123">This cmdlet gets information about logical gateways in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="6a658-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a658-124">-DefaultProfile</span></span>
<span data-ttu-id="6a658-125">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="6a658-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6a658-126">-Name</span><span class="sxs-lookup"><span data-stu-id="6a658-126">-Name</span></span>
<span data-ttu-id="6a658-127">Annak a logikai átjárónak a nevét adja meg, amelyről információt kell kapni.</span><span class="sxs-lookup"><span data-stu-id="6a658-127">Specifies the name of the logical gateway about which to get information.</span></span>

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

### <span data-ttu-id="6a658-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a658-128">-ResourceGroupName</span></span>
<span data-ttu-id="6a658-129">Egy Azure-erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6a658-129">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="6a658-130">Ez a parancsmag információt kap a paraméter által megadott csoporthoz tartozó logikai átjárókról.</span><span class="sxs-lookup"><span data-stu-id="6a658-130">This cmdlet gets information about logical gateways that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="6a658-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a658-131">CommonParameters</span></span>
<span data-ttu-id="6a658-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a658-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a658-133">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a658-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a658-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6a658-134">INPUTS</span></span>

### <span data-ttu-id="6a658-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="6a658-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="6a658-136">System.String</span><span class="sxs-lookup"><span data-stu-id="6a658-136">System.String</span></span>

## <span data-ttu-id="6a658-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6a658-137">OUTPUTS</span></span>

### <span data-ttu-id="6a658-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="6a658-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span></span>

## <span data-ttu-id="6a658-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6a658-139">NOTES</span></span>
* <span data-ttu-id="6a658-140">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, adatok, faktorok</span><span class="sxs-lookup"><span data-stu-id="6a658-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="6a658-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6a658-141">RELATED LINKS</span></span>

[<span data-ttu-id="6a658-142">New-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="6a658-142">New-AzDataFactoryGateway</span></span>](./New-AzDataFactoryGateway.md)

[<span data-ttu-id="6a658-143">Remove-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="6a658-143">Remove-AzDataFactoryGateway</span></span>](./Remove-AzDataFactoryGateway.md)

[<span data-ttu-id="6a658-144">Set-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="6a658-144">Set-AzDataFactoryGateway</span></span>](./Set-AzDataFactoryGateway.md)


