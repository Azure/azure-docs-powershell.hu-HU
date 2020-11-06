---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 46efba5e2ab9a5c51172264b343b0f4f2b508065
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/23/2019
ms.locfileid: "93490451"
---
# <span data-ttu-id="e380c-101">Import-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="e380c-101">Import-AzureRmContext</span></span>

## <span data-ttu-id="e380c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e380c-102">SYNOPSIS</span></span>
<span data-ttu-id="e380c-103">Azure-hitelesítési adatok betöltése egy fájlból.</span><span class="sxs-lookup"><span data-stu-id="e380c-103">Loads Azure authentication information from a file.</span></span>

## <span data-ttu-id="e380c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e380c-104">SYNTAX</span></span>

### <span data-ttu-id="e380c-105">InMemoryProfile</span><span class="sxs-lookup"><span data-stu-id="e380c-105">InMemoryProfile</span></span>
```
Import-AzureRmContext [-AzureContext] <AzureRmProfile> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="e380c-106">ProfileFromDisk</span><span class="sxs-lookup"><span data-stu-id="e380c-106">ProfileFromDisk</span></span>
```
Import-AzureRmContext [-Path] <String> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="e380c-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="e380c-107">DESCRIPTION</span></span>
<span data-ttu-id="e380c-108">A Import-AzureRmContext parancsmag az Azure-környezet és-környezet beállításához betölti a fájlok hitelesítési adatait.</span><span class="sxs-lookup"><span data-stu-id="e380c-108">The Import-AzureRmContext cmdlet loads authentication information from a file to set the Azure environment and context.</span></span>
<span data-ttu-id="e380c-109">Az aktuális munkamenetben futtatott parancsmagok ezekkel az információkkal hitelesíthetők az Azure Resource Manager kérései között.</span><span class="sxs-lookup"><span data-stu-id="e380c-109">Cmdlets that you run in the current session use this information to authenticate requests to Azure Resource Manager.</span></span>

## <span data-ttu-id="e380c-110">Példák</span><span class="sxs-lookup"><span data-stu-id="e380c-110">EXAMPLES</span></span>

### <span data-ttu-id="e380c-111">1. példa: környezet importálása AzureRmProfile</span><span class="sxs-lookup"><span data-stu-id="e380c-111">Example 1: Importing a context from a AzureRmProfile</span></span>
```
PS C:\> Import-AzureRmContext -AzureContext (Add-AzureRmAccount)

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

<span data-ttu-id="e380c-112">Ebben a példában egy olyan környezetet importál egy PSAzureProfile, amely át lett adva a parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="e380c-112">This example imports a context from a PSAzureProfile that is passed through to the cmdlet.</span></span>

### <span data-ttu-id="e380c-113">2. példa: környezet importálása JSON-fájlból</span><span class="sxs-lookup"><span data-stu-id="e380c-113">Example 2: Importing a context from a JSON file</span></span>
```
PS C:\> Import-AzureRmContext -Path C:\test.json

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

<span data-ttu-id="e380c-114">Ebben a példában egy JSON-fájl egy olyan környezetét jelöli ki, amely át lett adva a parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="e380c-114">This example selects a context from a JSON file that is passed through to the cmdlet.</span></span>
<span data-ttu-id="e380c-115">Ez a JSON-fájl hozható létre az import-AzureRmContext-ből.</span><span class="sxs-lookup"><span data-stu-id="e380c-115">This JSON file can be created from Import-AzureRmContext.</span></span>

## <span data-ttu-id="e380c-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e380c-116">PARAMETERS</span></span>

### <span data-ttu-id="e380c-117">-AzureContext</span><span class="sxs-lookup"><span data-stu-id="e380c-117">-AzureContext</span></span>
<span data-ttu-id="e380c-118">Azt az Azure-környezetet adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="e380c-118">Specifies the Azure context from which this cmdlet reads.</span></span>
<span data-ttu-id="e380c-119">Ha nem ad meg környezetet, a parancsmag a helyi alapértelmezett környezetből olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="e380c-119">If you do not specify a context, this cmdlet reads from the local default context.</span></span>

```yaml
Type: AzureRmProfile
Parameter Sets: InMemoryProfile
Aliases: Profile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e380c-120">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="e380c-120">-Path</span></span>
<span data-ttu-id="e380c-121">A Save-AzureRMContext paranccsal mentett környezeti információk elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="e380c-121">Specifies the path to context information saved by using Save-AzureRMContext.</span></span>

```yaml
Type: String
Parameter Sets: ProfileFromDisk
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e380c-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e380c-122">-Confirm</span></span>
<span data-ttu-id="e380c-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e380c-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e380c-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e380c-124">-WhatIf</span></span>
<span data-ttu-id="e380c-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e380c-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e380c-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e380c-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="e380c-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e380c-127">INPUTS</span></span>

### <span data-ttu-id="e380c-128">Microsoft. Azure. commands. Common. Authentication. models. AzureRMProfile</span><span class="sxs-lookup"><span data-stu-id="e380c-128">Microsoft.Azure.Commands.Common.Authentication.Models.AzureRMProfile</span></span>
<span data-ttu-id="e380c-129">System. String</span><span class="sxs-lookup"><span data-stu-id="e380c-129">System.String</span></span>

## <span data-ttu-id="e380c-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e380c-130">OUTPUTS</span></span>

### <span data-ttu-id="e380c-131">Microsoft. Azure. Command. profil. models. PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="e380c-131">Microsoft.Azure.Commands.Profile.Models.PSAzureProfile</span></span>

## <span data-ttu-id="e380c-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e380c-132">NOTES</span></span>

## <span data-ttu-id="e380c-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e380c-133">RELATED LINKS</span></span>

