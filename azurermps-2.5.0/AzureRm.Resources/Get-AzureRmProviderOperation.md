---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6424B740-DBFB-490C-AEAA-EDD60952B435
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermprovideroperation
schema: 2.0.0
ms.openlocfilehash: 1274b04ed85917a9c1e185bfbef6307eaedecc05
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849498"
---
# <span data-ttu-id="d5ecf-101">Get-AzureRmProviderOperation</span><span class="sxs-lookup"><span data-stu-id="d5ecf-101">Get-AzureRmProviderOperation</span></span>

## <span data-ttu-id="d5ecf-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d5ecf-102">SYNOPSIS</span></span>
<span data-ttu-id="d5ecf-103">Olyan Azure Resource Provider műveleteit kapja meg, amelyek az Azure RBAC segítségével biztonságossá tehetők.</span><span class="sxs-lookup"><span data-stu-id="d5ecf-103">Gets the operations for an Azure resource provider that are securable using Azure RBAC.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d5ecf-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d5ecf-104">SYNTAX</span></span>

```
Get-AzureRmProviderOperation [[-OperationSearchString] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d5ecf-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d5ecf-105">DESCRIPTION</span></span>
<span data-ttu-id="d5ecf-106">Az Get-AzureRmProviderOperation az Azure Resource Providers által kitett műveleteket kapja meg.</span><span class="sxs-lookup"><span data-stu-id="d5ecf-106">The Get-AzureRmProviderOperation gets the operations exposed by Azure resource providers.</span></span>
<span data-ttu-id="d5ecf-107">A műveletek létrehozhatók egyéni szerepkörök az Azure RBAC-ban.</span><span class="sxs-lookup"><span data-stu-id="d5ecf-107">Operations can be composed to create custom roles in Azure RBAC.</span></span>
<span data-ttu-id="d5ecf-108">A parancs beírja a kívánt műveleti keresési karakterláncot (esetleges helyettesítő *karakterrel ()), amely meghatározza a megjelenítendő műveletek részleteit. A Get-AzureRmProviderOperation \* segítségével minden Azure Resource Provider művelethez hozzáférhet. Használja Get-AzureRmProviderOperation Microsoft. kiszámítás/* a Microsoft összes műveletének beszerzése lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="d5ecf-108">The command takes as input an operation search string (with possible wildcard( *) character(s)) which determines the operations details to display. Use Get-AzureRmProviderOperation \* to get all operations for all Azure resource providers. Use Get-AzureRmProviderOperation Microsoft.Compute/* to get all operations of Microsoft.Compute resource provider.</span></span>

## <span data-ttu-id="d5ecf-109">Példák</span><span class="sxs-lookup"><span data-stu-id="d5ecf-109">EXAMPLES</span></span>

### <span data-ttu-id="d5ecf-110">Minden művelet beolvasása minden szolgáltatónál</span><span class="sxs-lookup"><span data-stu-id="d5ecf-110">Get all actions for all providers</span></span>
```
PS C:\> Get-AzureRmProviderOperation *
```

### <span data-ttu-id="d5ecf-111">Műveletek beszerzése egy adott erőforrás-szolgáltatónál</span><span class="sxs-lookup"><span data-stu-id="d5ecf-111">Get actions for a particular resource provider</span></span>
```
PS C:\> Get-AzureRmProviderOperation Microsoft.Insights/*
```

### <span data-ttu-id="d5ecf-112">A virtuális gépeken végezhető műveletek beolvasása</span><span class="sxs-lookup"><span data-stu-id="d5ecf-112">Get all actions that can be performed on virtual machines</span></span>
```
PS C:\> Get-AzureRmProviderOperation */virtualMachines/*
```

## <span data-ttu-id="d5ecf-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d5ecf-113">PARAMETERS</span></span>

### <span data-ttu-id="d5ecf-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5ecf-114">-DefaultProfile</span></span>
<span data-ttu-id="d5ecf-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="d5ecf-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d5ecf-116">-OperationSearchString</span><span class="sxs-lookup"><span data-stu-id="d5ecf-116">-OperationSearchString</span></span>
<span data-ttu-id="d5ecf-117">A művelet keresési karakterlánca (esetleges helyettesítő karakterekkel (\*)</span><span class="sxs-lookup"><span data-stu-id="d5ecf-117">The operation search string (with possible wildcard (\*) characters)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 0
Default value: "*"
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d5ecf-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5ecf-118">CommonParameters</span></span>
<span data-ttu-id="d5ecf-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d5ecf-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5ecf-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5ecf-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5ecf-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d5ecf-121">INPUTS</span></span>

### <span data-ttu-id="d5ecf-122">System. String</span><span class="sxs-lookup"><span data-stu-id="d5ecf-122">System.String</span></span>
<span data-ttu-id="d5ecf-123">Paraméterek: OperationSearchString (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d5ecf-123">Parameters: OperationSearchString (ByValue)</span></span>

## <span data-ttu-id="d5ecf-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d5ecf-124">OUTPUTS</span></span>

### <span data-ttu-id="d5ecf-125">Microsoft. Azure. Command. Resources. models. PSResourceProviderOperation</span><span class="sxs-lookup"><span data-stu-id="d5ecf-125">Microsoft.Azure.Commands.Resources.Models.PSResourceProviderOperation</span></span>

## <span data-ttu-id="d5ecf-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d5ecf-126">NOTES</span></span>
<span data-ttu-id="d5ecf-127">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, erőforrás, csoport, sablon, központi telepítő</span><span class="sxs-lookup"><span data-stu-id="d5ecf-127">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="d5ecf-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d5ecf-128">RELATED LINKS</span></span>
