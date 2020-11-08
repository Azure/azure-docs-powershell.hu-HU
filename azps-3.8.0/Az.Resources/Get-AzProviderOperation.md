---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6424B740-DBFB-490C-AEAA-EDD60952B435
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azprovideroperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzProviderOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzProviderOperation.md
ms.openlocfilehash: 1ee29a4183dd78e9ced6d48e5f52c724e1b9a985
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012617"
---
# <span data-ttu-id="3dc34-101">Get-AzProviderOperation</span><span class="sxs-lookup"><span data-stu-id="3dc34-101">Get-AzProviderOperation</span></span>

## <span data-ttu-id="3dc34-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3dc34-102">SYNOPSIS</span></span>
<span data-ttu-id="3dc34-103">Olyan Azure Resource Provider műveleteit kapja meg, amelyek az Azure RBAC segítségével biztonságossá tehetők.</span><span class="sxs-lookup"><span data-stu-id="3dc34-103">Gets the operations for an Azure resource provider that are securable using Azure RBAC.</span></span>

## <span data-ttu-id="3dc34-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3dc34-104">SYNTAX</span></span>

```
Get-AzProviderOperation [[-OperationSearchString] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3dc34-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3dc34-105">DESCRIPTION</span></span>
<span data-ttu-id="3dc34-106">Az Get-AzProviderOperation az Azure Resource Providers által kitett műveleteket kapja meg.</span><span class="sxs-lookup"><span data-stu-id="3dc34-106">The Get-AzProviderOperation gets the operations exposed by Azure resource providers.</span></span>
<span data-ttu-id="3dc34-107">A műveletek létrehozhatók egyéni szerepkörök az Azure RBAC-ban.</span><span class="sxs-lookup"><span data-stu-id="3dc34-107">Operations can be composed to create custom roles in Azure RBAC.</span></span>
<span data-ttu-id="3dc34-108">A parancs beírja a kívánt műveleti keresési karakterláncot (esetleges helyettesítő *karakterrel ()), amely meghatározza a megjelenítendő műveletek részleteit. A Get-AzProviderOperation \* segítségével minden Azure Resource Provider művelethez hozzáférhet. Használja Get-AzProviderOperation Microsoft. kiszámítás/* a Microsoft összes műveletének beszerzése lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="3dc34-108">The command takes as input an operation search string (with possible wildcard( *) character(s)) which determines the operations details to display. Use Get-AzProviderOperation \* to get all operations for all Azure resource providers. Use Get-AzProviderOperation Microsoft.Compute/* to get all operations of Microsoft.Compute resource provider.</span></span>

## <span data-ttu-id="3dc34-109">Példák</span><span class="sxs-lookup"><span data-stu-id="3dc34-109">EXAMPLES</span></span>

### <span data-ttu-id="3dc34-110">Minden művelet beolvasása minden szolgáltatónál</span><span class="sxs-lookup"><span data-stu-id="3dc34-110">Get all actions for all providers</span></span>
```
PS C:\> Get-AzProviderOperation *
```

### <span data-ttu-id="3dc34-111">Műveletek beszerzése egy adott erőforrás-szolgáltatónál</span><span class="sxs-lookup"><span data-stu-id="3dc34-111">Get actions for a particular resource provider</span></span>
```
PS C:\> Get-AzProviderOperation Microsoft.Insights/*
```

### <span data-ttu-id="3dc34-112">A virtuális gépeken végezhető műveletek beolvasása</span><span class="sxs-lookup"><span data-stu-id="3dc34-112">Get all actions that can be performed on virtual machines</span></span>
```
PS C:\> Get-AzProviderOperation */virtualMachines/*
```

## <span data-ttu-id="3dc34-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3dc34-113">PARAMETERS</span></span>

### <span data-ttu-id="3dc34-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3dc34-114">-DefaultProfile</span></span>
<span data-ttu-id="3dc34-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="3dc34-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3dc34-116">-OperationSearchString</span><span class="sxs-lookup"><span data-stu-id="3dc34-116">-OperationSearchString</span></span>
<span data-ttu-id="3dc34-117">A művelet keresési karakterlánca (esetleges helyettesítő karakterekkel (\*)</span><span class="sxs-lookup"><span data-stu-id="3dc34-117">The operation search string (with possible wildcard (\*) characters)</span></span>

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

### <span data-ttu-id="3dc34-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3dc34-118">CommonParameters</span></span>
<span data-ttu-id="3dc34-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3dc34-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3dc34-120">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="3dc34-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3dc34-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3dc34-121">INPUTS</span></span>

### <span data-ttu-id="3dc34-122">System. String</span><span class="sxs-lookup"><span data-stu-id="3dc34-122">System.String</span></span>

## <span data-ttu-id="3dc34-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3dc34-123">OUTPUTS</span></span>

### <span data-ttu-id="3dc34-124">Microsoft. Azure. Command. Resources. models. PSResourceProviderOperation</span><span class="sxs-lookup"><span data-stu-id="3dc34-124">Microsoft.Azure.Commands.Resources.Models.PSResourceProviderOperation</span></span>

## <span data-ttu-id="3dc34-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3dc34-125">NOTES</span></span>
<span data-ttu-id="3dc34-126">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, erőforrás, csoport, sablon, központi telepítő</span><span class="sxs-lookup"><span data-stu-id="3dc34-126">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="3dc34-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3dc34-127">RELATED LINKS</span></span>
