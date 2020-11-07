---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6424B740-DBFB-490C-AEAA-EDD60952B435
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmProviderOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmProviderOperation.md
ms.openlocfilehash: d4e58e1fc2da68d9293afa27072a4cf32023f661
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679044"
---
# <span data-ttu-id="d20b6-101">Get-AzureRmProviderOperation</span><span class="sxs-lookup"><span data-stu-id="d20b6-101">Get-AzureRmProviderOperation</span></span>

## <span data-ttu-id="d20b6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d20b6-102">SYNOPSIS</span></span>
<span data-ttu-id="d20b6-103">Olyan Azure Resource Provider műveleteit kapja meg, amelyek az Azure RBAC segítségével biztonságossá tehetők.</span><span class="sxs-lookup"><span data-stu-id="d20b6-103">Gets the operations for an Azure resource provider that are securable using Azure RBAC.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d20b6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d20b6-104">SYNTAX</span></span>

```
Get-AzureRmProviderOperation [-OperationSearchString] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d20b6-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d20b6-105">DESCRIPTION</span></span>
<span data-ttu-id="d20b6-106">Az Get-AzureRmProviderOperation az Azure Resource Providers által kitett műveleteket kapja meg.</span><span class="sxs-lookup"><span data-stu-id="d20b6-106">The Get-AzureRmProviderOperation gets the operations exposed by Azure resource providers.</span></span>
<span data-ttu-id="d20b6-107">A műveletek létrehozhatók egyéni szerepkörök az Azure RBAC-ban.</span><span class="sxs-lookup"><span data-stu-id="d20b6-107">Operations can be composed to create custom roles in Azure RBAC.</span></span>
<span data-ttu-id="d20b6-108">A parancs a művelet keresési karakterláncát adja meg, amely a megjelenített műveletek részleteit határozza meg.</span><span class="sxs-lookup"><span data-stu-id="d20b6-108">The command takes as input an operation search string (with possible wildcard(\*) character(s)) which determines the operations details to display.</span></span>

<span data-ttu-id="d20b6-109">A Get-AzureRmProviderOperation \* segítségével minden Azure Resource Provider művelethez hozzáférhet.</span><span class="sxs-lookup"><span data-stu-id="d20b6-109">Use Get-AzureRmProviderOperation \* to get all operations for all Azure resource providers.</span></span>

<span data-ttu-id="d20b6-110">Használja Get-AzureRmProviderOperation Microsoft. számítási/\* lehetőséget a Microsoft összes műveletének beszerzéséhez. az erőforrás-szolgáltató kiszámítása.</span><span class="sxs-lookup"><span data-stu-id="d20b6-110">Use Get-AzureRmProviderOperation Microsoft.Compute/\* to get all operations of Microsoft.Compute resource provider.</span></span>

## <span data-ttu-id="d20b6-111">Példák</span><span class="sxs-lookup"><span data-stu-id="d20b6-111">EXAMPLES</span></span>

### <span data-ttu-id="d20b6-112">--------------------------A minden szolgáltató összes műveletének beszerzése--------------------------</span><span class="sxs-lookup"><span data-stu-id="d20b6-112">--------------------------  Get all actions for all providers  --------------------------</span></span>
```
PS C:\> Get-AzureRmProviderOperation *
```

### <span data-ttu-id="d20b6-113">--------------------------Beszerzése egy adott erőforrás-szolgáltatónál--------------------------</span><span class="sxs-lookup"><span data-stu-id="d20b6-113">--------------------------  Get actions for a particular resource provider  --------------------------</span></span>
```
PS C:\> Get-AzureRmProviderOperation Microsoft.Insights/*
```

### <span data-ttu-id="d20b6-114">--------------------------A virtuális gépeken végrehajtható összes művelet beszerzése--------------------------</span><span class="sxs-lookup"><span data-stu-id="d20b6-114">--------------------------  Get all actions that can be performed on virtual machines  --------------------------</span></span>
```
PS C:\> Get-AzureRmProviderOperation */virtualMachines/*
```

## <span data-ttu-id="d20b6-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d20b6-115">PARAMETERS</span></span>

### <span data-ttu-id="d20b6-116">-OperationSearchString</span><span class="sxs-lookup"><span data-stu-id="d20b6-116">-OperationSearchString</span></span>
<span data-ttu-id="d20b6-117">A művelet keresési karakterlánca (esetleges helyettesítő karakterekkel (\*)</span><span class="sxs-lookup"><span data-stu-id="d20b6-117">The operation search string (with possible wildcard (\*) characters)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d20b6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d20b6-118">-DefaultProfile</span></span>
<span data-ttu-id="d20b6-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d20b6-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d20b6-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d20b6-120">CommonParameters</span></span>
<span data-ttu-id="d20b6-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d20b6-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d20b6-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d20b6-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d20b6-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d20b6-123">INPUTS</span></span>

### <span data-ttu-id="d20b6-124">Karakterlánc</span><span class="sxs-lookup"><span data-stu-id="d20b6-124">String</span></span>
<span data-ttu-id="d20b6-125">A ' OperationSearchString ' paraméter a "string" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="d20b6-125">Parameter 'OperationSearchString' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="d20b6-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d20b6-126">OUTPUTS</span></span>

### <span data-ttu-id="d20b6-127">Microsoft. Azure. Command. Resources. models. PSResourceProviderOperation</span><span class="sxs-lookup"><span data-stu-id="d20b6-127">Microsoft.Azure.Commands.Resources.Models.PSResourceProviderOperation</span></span>

## <span data-ttu-id="d20b6-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d20b6-128">NOTES</span></span>
<span data-ttu-id="d20b6-129">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, erőforrás, csoport, sablon, központi telepítő</span><span class="sxs-lookup"><span data-stu-id="d20b6-129">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="d20b6-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d20b6-130">RELATED LINKS</span></span>

