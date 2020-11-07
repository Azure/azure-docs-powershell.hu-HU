---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6424B740-DBFB-490C-AEAA-EDD60952B435
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azprovideroperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzProviderOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzProviderOperation.md
ms.openlocfilehash: 21e1af2a36478f2e0b8e470660d0fbe2539a396e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843429"
---
# <span data-ttu-id="a9d33-101">Get-AzProviderOperation</span><span class="sxs-lookup"><span data-stu-id="a9d33-101">Get-AzProviderOperation</span></span>

## <span data-ttu-id="a9d33-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a9d33-102">SYNOPSIS</span></span>
<span data-ttu-id="a9d33-103">Olyan Azure Resource Provider műveleteit kapja meg, amelyek az Azure RBAC segítségével biztonságossá tehetők.</span><span class="sxs-lookup"><span data-stu-id="a9d33-103">Gets the operations for an Azure resource provider that are securable using Azure RBAC.</span></span>

## <span data-ttu-id="a9d33-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a9d33-104">SYNTAX</span></span>

```
Get-AzProviderOperation [[-OperationSearchString] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a9d33-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a9d33-105">DESCRIPTION</span></span>
<span data-ttu-id="a9d33-106">Az Get-AzProviderOperation az Azure Resource Providers által kitett műveleteket kapja meg.</span><span class="sxs-lookup"><span data-stu-id="a9d33-106">The Get-AzProviderOperation gets the operations exposed by Azure resource providers.</span></span>
<span data-ttu-id="a9d33-107">A műveletek létrehozhatók egyéni szerepkörök az Azure RBAC-ban.</span><span class="sxs-lookup"><span data-stu-id="a9d33-107">Operations can be composed to create custom roles in Azure RBAC.</span></span>
<span data-ttu-id="a9d33-108">A parancs beírja a kívánt műveleti keresési karakterláncot (esetleges helyettesítő *karakterrel ()), amely meghatározza a megjelenítendő műveletek részleteit. A Get-AzProviderOperation \* segítségével minden Azure Resource Provider művelethez hozzáférhet. Használja Get-AzProviderOperation Microsoft. kiszámítás/* a Microsoft összes műveletének beszerzése lehetőséget.</span><span class="sxs-lookup"><span data-stu-id="a9d33-108">The command takes as input an operation search string (with possible wildcard( *) character(s)) which determines the operations details to display. Use Get-AzProviderOperation \* to get all operations for all Azure resource providers. Use Get-AzProviderOperation Microsoft.Compute/* to get all operations of Microsoft.Compute resource provider.</span></span>

## <span data-ttu-id="a9d33-109">Példák</span><span class="sxs-lookup"><span data-stu-id="a9d33-109">EXAMPLES</span></span>

### <span data-ttu-id="a9d33-110">Minden művelet beolvasása minden szolgáltatónál</span><span class="sxs-lookup"><span data-stu-id="a9d33-110">Get all actions for all providers</span></span>
```
PS C:\> Get-AzProviderOperation *
```

### <span data-ttu-id="a9d33-111">Műveletek beszerzése egy adott erőforrás-szolgáltatónál</span><span class="sxs-lookup"><span data-stu-id="a9d33-111">Get actions for a particular resource provider</span></span>
```
PS C:\> Get-AzProviderOperation Microsoft.Insights/*
```

### <span data-ttu-id="a9d33-112">A virtuális gépeken végezhető műveletek beolvasása</span><span class="sxs-lookup"><span data-stu-id="a9d33-112">Get all actions that can be performed on virtual machines</span></span>
```
PS C:\> Get-AzProviderOperation */virtualMachines/*
```

## <span data-ttu-id="a9d33-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a9d33-113">PARAMETERS</span></span>

### <span data-ttu-id="a9d33-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9d33-114">-DefaultProfile</span></span>
<span data-ttu-id="a9d33-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="a9d33-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9d33-116">-OperationSearchString</span><span class="sxs-lookup"><span data-stu-id="a9d33-116">-OperationSearchString</span></span>
<span data-ttu-id="a9d33-117">A művelet keresési karakterlánca (esetleges helyettesítő karakterekkel (\*)</span><span class="sxs-lookup"><span data-stu-id="a9d33-117">The operation search string (with possible wildcard (\*) characters)</span></span>

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

### <span data-ttu-id="a9d33-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9d33-118">CommonParameters</span></span>
<span data-ttu-id="a9d33-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a9d33-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9d33-120">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9d33-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9d33-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a9d33-121">INPUTS</span></span>

### <span data-ttu-id="a9d33-122">System. String</span><span class="sxs-lookup"><span data-stu-id="a9d33-122">System.String</span></span>
<span data-ttu-id="a9d33-123">Paraméterek: OperationSearchString (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a9d33-123">Parameters: OperationSearchString (ByValue)</span></span>

## <span data-ttu-id="a9d33-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a9d33-124">OUTPUTS</span></span>

### <span data-ttu-id="a9d33-125">Microsoft. Azure. Command. Resources. models. PSResourceProviderOperation</span><span class="sxs-lookup"><span data-stu-id="a9d33-125">Microsoft.Azure.Commands.Resources.Models.PSResourceProviderOperation</span></span>

## <span data-ttu-id="a9d33-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a9d33-126">NOTES</span></span>
<span data-ttu-id="a9d33-127">Kulcsszavak: Azure, az, kar, erőforrás, kezelés, vezető, erőforrás, csoport, sablon, központi telepítő</span><span class="sxs-lookup"><span data-stu-id="a9d33-127">Keywords: azure, Az, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="a9d33-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a9d33-128">RELATED LINKS</span></span>
