---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6424B740-DBFB-490C-AEAA-EDD60952B435
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azprovideroperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzProviderOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzProviderOperation.md
ms.openlocfilehash: bffe2874effb99b3fbcca77888a3108bc3798311
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466512"
---
# <span data-ttu-id="61ca0-101">Get-AzProviderOperation</span><span class="sxs-lookup"><span data-stu-id="61ca0-101">Get-AzProviderOperation</span></span>

## <span data-ttu-id="61ca0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61ca0-102">SYNOPSIS</span></span>
<span data-ttu-id="61ca0-103">Egy Azure-erőforrás-szolgáltató azure RBAC-n keresztül biztonságos műveleteit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="61ca0-103">Gets the operations for an Azure resource provider that are securable using Azure RBAC.</span></span>

## <span data-ttu-id="61ca0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="61ca0-104">SYNTAX</span></span>

```
Get-AzProviderOperation [[-OperationSearchString] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="61ca0-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="61ca0-105">DESCRIPTION</span></span>
<span data-ttu-id="61ca0-106">A Get-AzProviderOperation azure-erőforrás-szolgáltatók számára elérhetővé teszi a műveleteket.</span><span class="sxs-lookup"><span data-stu-id="61ca0-106">The Get-AzProviderOperation gets the operations exposed by Azure resource providers.</span></span>
<span data-ttu-id="61ca0-107">Az Azure RBAC-ban egyéni szerepkörök létrehozásához létrehozható műveletek.</span><span class="sxs-lookup"><span data-stu-id="61ca0-107">Operations can be composed to create custom roles in Azure RBAC.</span></span>
<span data-ttu-id="61ca0-108">A parancs bemeneti karakterláncként (lehetséges helyettesítő karakter(ek) karaktert tartalmaz, amely meghatározza a megjelenítendő műveletek *részleteit. A Get-AzProviderOperation \* használatával az összes Azure-erőforrás-szolgáltató összes műveletét lekérte. A Get-AzProviderOperation.Compute/* segítségével lekérte a Microsoft.Compute erőforrás-szolgáltató összes műveletét.</span><span class="sxs-lookup"><span data-stu-id="61ca0-108">The command takes as input an operation search string (with possible wildcard(*) character(s)) which determines the operations details to display. Use Get-AzProviderOperation \* to get all operations for all Azure resource providers. Use Get-AzProviderOperation Microsoft.Compute/* to get all operations of Microsoft.Compute resource provider.</span></span>

## <span data-ttu-id="61ca0-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="61ca0-109">EXAMPLES</span></span>

### <span data-ttu-id="61ca0-110">1. példa: Az összes művelet lekérte az összes szolgáltatót</span><span class="sxs-lookup"><span data-stu-id="61ca0-110">Example 1: Get all actions for all providers</span></span>
```powershell
PS C:\> Get-AzProviderOperation *
```

### <span data-ttu-id="61ca0-111">2. példa: Adott erőforrás-szolgáltatóhoz szükséges műveletek lekérte</span><span class="sxs-lookup"><span data-stu-id="61ca0-111">Example 2: Get actions for a particular resource provider</span></span>
```powershell
PS C:\> Get-AzProviderOperation Microsoft.Insights/*
```

### <span data-ttu-id="61ca0-112">3. példa: A virtuális gépeken elvégezhető összes művelet lekérte</span><span class="sxs-lookup"><span data-stu-id="61ca0-112">Example 3: Get all actions that can be performed on virtual machines</span></span>
```powershell
PS C:\> Get-AzProviderOperation */virtualMachines/*
```

## <span data-ttu-id="61ca0-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="61ca0-113">PARAMETERS</span></span>

### <span data-ttu-id="61ca0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61ca0-114">-DefaultProfile</span></span>
<span data-ttu-id="61ca0-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="61ca0-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="61ca0-116">-OperationSearchString</span><span class="sxs-lookup"><span data-stu-id="61ca0-116">-OperationSearchString</span></span>
<span data-ttu-id="61ca0-117">A művelet keresési karakterlánca (lehetséges helyettesítő karakterekkel (\*) karakterekkel)</span><span class="sxs-lookup"><span data-stu-id="61ca0-117">The operation search string (with possible wildcard (\*) characters)</span></span>

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

### <span data-ttu-id="61ca0-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61ca0-118">CommonParameters</span></span>
<span data-ttu-id="61ca0-119">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61ca0-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61ca0-120">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="61ca0-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61ca0-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="61ca0-121">INPUTS</span></span>

### <span data-ttu-id="61ca0-122">System.String</span><span class="sxs-lookup"><span data-stu-id="61ca0-122">System.String</span></span>

## <span data-ttu-id="61ca0-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="61ca0-123">OUTPUTS</span></span>

### <span data-ttu-id="61ca0-124">Microsoft.Azure.Commands.Resources.Models.PSResourceProviderOperation</span><span class="sxs-lookup"><span data-stu-id="61ca0-124">Microsoft.Azure.Commands.Resources.Models.PSResourceProviderOperation</span></span>

## <span data-ttu-id="61ca0-125">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="61ca0-125">NOTES</span></span>
<span data-ttu-id="61ca0-126">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, erőforrás, csoport, sablon, telepítés</span><span class="sxs-lookup"><span data-stu-id="61ca0-126">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="61ca0-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="61ca0-127">RELATED LINKS</span></span>
