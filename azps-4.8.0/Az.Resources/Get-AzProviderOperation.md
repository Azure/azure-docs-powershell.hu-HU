---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6424B740-DBFB-490C-AEAA-EDD60952B435
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azprovideroperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzProviderOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzProviderOperation.md
ms.openlocfilehash: bffe2874effb99b3fbcca77888a3108bc3798311
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181436"
---
# <span data-ttu-id="94e69-101">Get-AzProviderOperation</span><span class="sxs-lookup"><span data-stu-id="94e69-101">Get-AzProviderOperation</span></span>

## <span data-ttu-id="94e69-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="94e69-102">SYNOPSIS</span></span>
<span data-ttu-id="94e69-103">Olyan Azure Resource Provider műveleteit kapja meg, amelyek az Azure RBAC segítségével biztonságossá tehetők.</span><span class="sxs-lookup"><span data-stu-id="94e69-103">Gets the operations for an Azure resource provider that are securable using Azure RBAC.</span></span>

## <span data-ttu-id="94e69-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="94e69-104">SYNTAX</span></span>

```
Get-AzProviderOperation [[-OperationSearchString] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="94e69-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="94e69-105">DESCRIPTION</span></span>
<span data-ttu-id="94e69-106">Az Get-AzProviderOperation az Azure Resource Providers által kitett műveleteket kapja meg.</span><span class="sxs-lookup"><span data-stu-id="94e69-106">The Get-AzProviderOperation gets the operations exposed by Azure resource providers.</span></span>
<span data-ttu-id="94e69-107">A műveletek létrehozhatók egyéni szerepkörök az Azure RBAC-ban.</span><span class="sxs-lookup"><span data-stu-id="94e69-107">Operations can be composed to create custom roles in Azure RBAC.</span></span>
<span data-ttu-id="94e69-108">A parancs beírja a kívánt műveleti keresési karakterláncot (esetleges helyettesítő *karakterrel ()), amely meghatározza a megjelenítendő műveletek részleteit. A Get-AzProviderOperation \* segítségével minden Azure Resource Provider művelethez hozzáférhet. Használja Get-AzProviderOperation Microsoft. kiszámítás/* a Microsoft összes műveletének beszerzése lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="94e69-108">The command takes as input an operation search string (with possible wildcard( *) character(s)) which determines the operations details to display. Use Get-AzProviderOperation \* to get all operations for all Azure resource providers. Use Get-AzProviderOperation Microsoft.Compute/* to get all operations of Microsoft.Compute resource provider.</span></span>

## <span data-ttu-id="94e69-109">Példák</span><span class="sxs-lookup"><span data-stu-id="94e69-109">EXAMPLES</span></span>

### <span data-ttu-id="94e69-110">Példa 1: a minden szolgáltató minden műveletének beolvasása</span><span class="sxs-lookup"><span data-stu-id="94e69-110">Example 1: Get all actions for all providers</span></span>
```powershell
PS C:\> Get-AzProviderOperation *
```

### <span data-ttu-id="94e69-111">2. példa: műveletek beszerzése egy adott erőforrás-szolgáltatónál</span><span class="sxs-lookup"><span data-stu-id="94e69-111">Example 2: Get actions for a particular resource provider</span></span>
```powershell
PS C:\> Get-AzProviderOperation Microsoft.Insights/*
```

### <span data-ttu-id="94e69-112">3. példa: a virtuális gépeken végezhető műveletek beolvasása</span><span class="sxs-lookup"><span data-stu-id="94e69-112">Example 3: Get all actions that can be performed on virtual machines</span></span>
```powershell
PS C:\> Get-AzProviderOperation */virtualMachines/*
```

## <span data-ttu-id="94e69-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="94e69-113">PARAMETERS</span></span>

### <span data-ttu-id="94e69-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94e69-114">-DefaultProfile</span></span>
<span data-ttu-id="94e69-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="94e69-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="94e69-116">-OperationSearchString</span><span class="sxs-lookup"><span data-stu-id="94e69-116">-OperationSearchString</span></span>
<span data-ttu-id="94e69-117">A művelet keresési karakterlánca (esetleges helyettesítő karakterekkel (\*)</span><span class="sxs-lookup"><span data-stu-id="94e69-117">The operation search string (with possible wildcard (\*) characters)</span></span>

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

### <span data-ttu-id="94e69-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94e69-118">CommonParameters</span></span>
<span data-ttu-id="94e69-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="94e69-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94e69-120">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="94e69-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94e69-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="94e69-121">INPUTS</span></span>

### <span data-ttu-id="94e69-122">System. String</span><span class="sxs-lookup"><span data-stu-id="94e69-122">System.String</span></span>

## <span data-ttu-id="94e69-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="94e69-123">OUTPUTS</span></span>

### <span data-ttu-id="94e69-124">Microsoft. Azure. Command. Resources. models. PSResourceProviderOperation</span><span class="sxs-lookup"><span data-stu-id="94e69-124">Microsoft.Azure.Commands.Resources.Models.PSResourceProviderOperation</span></span>

## <span data-ttu-id="94e69-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="94e69-125">NOTES</span></span>
<span data-ttu-id="94e69-126">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, erőforrás, csoport, sablon, központi telepítő</span><span class="sxs-lookup"><span data-stu-id="94e69-126">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="94e69-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="94e69-127">RELATED LINKS</span></span>
