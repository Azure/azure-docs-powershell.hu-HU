---
external help file: ''
Module Name: Az.Communication
online version: https://docs.microsoft.com/powershell/module/az.communication/new-azcommunicationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/New-AzCommunicationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/New-AzCommunicationService.md
ms.openlocfilehash: 8382358e6bad15948ed8cdfeb904cf8c431bd131
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938953"
---
# <span data-ttu-id="a75de-101">New-AzCommunicationService</span><span class="sxs-lookup"><span data-stu-id="a75de-101">New-AzCommunicationService</span></span>

## <span data-ttu-id="a75de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a75de-102">SYNOPSIS</span></span>
<span data-ttu-id="a75de-103">Hozzon létre egy új CommunicationService szolgáltatást, vagy frissítsen egy meglévő CommunicationService szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="a75de-103">Create a new CommunicationService or update an existing CommunicationService.</span></span>

## <span data-ttu-id="a75de-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a75de-104">SYNTAX</span></span>

```
New-AzCommunicationService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DataLocation <String>] [-Location <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a75de-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a75de-105">DESCRIPTION</span></span>
<span data-ttu-id="a75de-106">Hozzon létre egy új CommunicationService szolgáltatást, vagy frissítsen egy meglévő CommunicationService szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="a75de-106">Create a new CommunicationService or update an existing CommunicationService.</span></span>

## <span data-ttu-id="a75de-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a75de-107">EXAMPLES</span></span>

### <span data-ttu-id="a75de-108">1. példa: ACS-erőforrás létrehozása</span><span class="sxs-lookup"><span data-stu-id="a75de-108">Example 1: Create a ACS resource</span></span>
```powershell
PS C:\> New-AzCommunicationService -ResourceGroupName ContosoResourceProvider1 -Name ContosoAcsResource1 -DataLocation UnitedStates -Location Global

Location Name           Type                                          AzureAsyncOperation
-------- ----           ----                                          -------------------
Global   ContosoAcsResource1 Microsoft.Communication/communicationServices
```

<span data-ttu-id="a75de-109">Létrehoz egy ACS-erőforrást a megadott paraméterekkel.</span><span class="sxs-lookup"><span data-stu-id="a75de-109">Creates a ACS resource using the specified parameters.</span></span>

## <span data-ttu-id="a75de-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a75de-110">PARAMETERS</span></span>

### <span data-ttu-id="a75de-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a75de-111">-AsJob</span></span>
<span data-ttu-id="a75de-112">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="a75de-112">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a75de-113">-DataLocation</span><span class="sxs-lookup"><span data-stu-id="a75de-113">-DataLocation</span></span>
<span data-ttu-id="a75de-114">Az a hely, ahol a kommunikációs szolgáltatás az adatokat tárolja.</span><span class="sxs-lookup"><span data-stu-id="a75de-114">The location where the communication service stores its data at rest.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a75de-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a75de-115">-DefaultProfile</span></span>
<span data-ttu-id="a75de-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a75de-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a75de-117">-Location</span><span class="sxs-lookup"><span data-stu-id="a75de-117">-Location</span></span>
<span data-ttu-id="a75de-118">Az Azure-hely, ahol a CommunicationService fut.</span><span class="sxs-lookup"><span data-stu-id="a75de-118">The Azure location where the CommunicationService is running.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a75de-119">-Name</span><span class="sxs-lookup"><span data-stu-id="a75de-119">-Name</span></span>
<span data-ttu-id="a75de-120">A CommunicationService erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="a75de-120">The name of the CommunicationService resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CommunicationServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a75de-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="a75de-121">-NoWait</span></span>
<span data-ttu-id="a75de-122">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="a75de-122">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a75de-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a75de-123">-ResourceGroupName</span></span>
<span data-ttu-id="a75de-124">Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="a75de-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="a75de-125">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="a75de-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a75de-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a75de-126">-SubscriptionId</span></span>
<span data-ttu-id="a75de-127">Olyan előfizetésazonosítót kap, amely egyedileg azonosítja a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="a75de-127">Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="a75de-128">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="a75de-128">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a75de-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="a75de-129">-Tag</span></span>
<span data-ttu-id="a75de-130">A szolgáltatás címkéi, amelyek az erőforrást leíró kulcsérték-párok listáját jelentik.</span><span class="sxs-lookup"><span data-stu-id="a75de-130">Tags of the service which is a list of key value pairs that describe the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a75de-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a75de-131">-Confirm</span></span>
<span data-ttu-id="a75de-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="a75de-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a75de-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a75de-133">-WhatIf</span></span>
<span data-ttu-id="a75de-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="a75de-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a75de-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a75de-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a75de-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a75de-136">CommonParameters</span></span>
<span data-ttu-id="a75de-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a75de-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a75de-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a75de-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a75de-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a75de-139">INPUTS</span></span>

## <span data-ttu-id="a75de-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a75de-140">OUTPUTS</span></span>

### <span data-ttu-id="a75de-141">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceResource</span><span class="sxs-lookup"><span data-stu-id="a75de-141">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceResource</span></span>

## <span data-ttu-id="a75de-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a75de-142">NOTES</span></span>

<span data-ttu-id="a75de-143">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="a75de-143">ALIASES</span></span>

## <span data-ttu-id="a75de-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a75de-144">RELATED LINKS</span></span>

