---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.cloudservice/set-azcloudserviceupdatedomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Set-AzCloudServiceUpdateDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Set-AzCloudServiceUpdateDomain.md
ms.openlocfilehash: 4b47992eb290c0a34ac2b368017d443051a6bb92
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937130"
---
# <span data-ttu-id="2a9e0-101">Set-AzCloudServiceUpdateDomain</span><span class="sxs-lookup"><span data-stu-id="2a9e0-101">Set-AzCloudServiceUpdateDomain</span></span>

## <span data-ttu-id="2a9e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2a9e0-102">SYNOPSIS</span></span>
<span data-ttu-id="2a9e0-103">Frissíti a szerepkörpéldányokat a megadott frissítési tartományban.</span><span class="sxs-lookup"><span data-stu-id="2a9e0-103">Updates the role instances in the specified update domain.</span></span>

## <span data-ttu-id="2a9e0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2a9e0-104">SYNTAX</span></span>

```
Set-AzCloudServiceUpdateDomain -CloudServiceName <String> -ResourceGroupName <String> -UpdateDomain <Int32>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="2a9e0-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2a9e0-105">DESCRIPTION</span></span>
<span data-ttu-id="2a9e0-106">Frissíti a szerepkörpéldányokat a megadott frissítési tartományban.</span><span class="sxs-lookup"><span data-stu-id="2a9e0-106">Updates the role instances in the specified update domain.</span></span>

## <span data-ttu-id="2a9e0-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2a9e0-107">EXAMPLES</span></span>

### <span data-ttu-id="2a9e0-108">1. példa: Szerepkörpéldány frissítése a frissítési tartományban</span><span class="sxs-lookup"><span data-stu-id="2a9e0-108">Example 1: Update role instance in update domain</span></span>
```powershell
PS C:\> Set-AzCloudServiceUpdateDomain -CloudServiceName "ContosoCS" -ResourceGroupName "ContosOrg" -UpdateDomain 0
```

<span data-ttu-id="2a9e0-109">Ez a parancs frissíti a ContosOrg nevű erőforráscsoporthoz tartozó ContosoCS nevű felhőszolgáltatás 0-s frissítési tartományában található szerepkörpéldányokat.</span><span class="sxs-lookup"><span data-stu-id="2a9e0-109">This command updates role instances in update domain 0 of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="2a9e0-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2a9e0-110">PARAMETERS</span></span>

### <span data-ttu-id="2a9e0-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2a9e0-111">-AsJob</span></span>
<span data-ttu-id="2a9e0-112">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="2a9e0-112">Run the command as a job</span></span>

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

### <span data-ttu-id="2a9e0-113">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="2a9e0-113">-CloudServiceName</span></span>
<span data-ttu-id="2a9e0-114">A felhőszolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="2a9e0-114">Name of the cloud service.</span></span>

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

### <span data-ttu-id="2a9e0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a9e0-115">-DefaultProfile</span></span>
<span data-ttu-id="2a9e0-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2a9e0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a9e0-117">-NoWait</span><span class="sxs-lookup"><span data-stu-id="2a9e0-117">-NoWait</span></span>
<span data-ttu-id="2a9e0-118">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="2a9e0-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="2a9e0-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2a9e0-119">-PassThru</span></span>
<span data-ttu-id="2a9e0-120">Igaz értéket ad vissza, ha a parancs sikeres</span><span class="sxs-lookup"><span data-stu-id="2a9e0-120">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="2a9e0-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a9e0-121">-ResourceGroupName</span></span>
<span data-ttu-id="2a9e0-122">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="2a9e0-122">Name of the resource group.</span></span>

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

### <span data-ttu-id="2a9e0-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2a9e0-123">-SubscriptionId</span></span>
<span data-ttu-id="2a9e0-124">Előfizetési hitelesítő adatok, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="2a9e0-124">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="2a9e0-125">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="2a9e0-125">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="2a9e0-126">-UpdateDomain</span><span class="sxs-lookup"><span data-stu-id="2a9e0-126">-UpdateDomain</span></span>
<span data-ttu-id="2a9e0-127">A frissítő tartományt azonosító egész értéket ad meg.</span><span class="sxs-lookup"><span data-stu-id="2a9e0-127">Specifies an integer value that identifies the update domain.</span></span>
<span data-ttu-id="2a9e0-128">A frissítési tartományokat nulla alapú index azonosítja: az első frissítési tartomány azonosítója 0, a második 1 és így tovább.</span><span class="sxs-lookup"><span data-stu-id="2a9e0-128">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a9e0-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2a9e0-129">-Confirm</span></span>
<span data-ttu-id="2a9e0-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="2a9e0-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a9e0-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a9e0-131">-WhatIf</span></span>
<span data-ttu-id="2a9e0-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="2a9e0-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a9e0-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2a9e0-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a9e0-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a9e0-134">CommonParameters</span></span>
<span data-ttu-id="2a9e0-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a9e0-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a9e0-136">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2a9e0-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a9e0-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2a9e0-137">INPUTS</span></span>

## <span data-ttu-id="2a9e0-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2a9e0-138">OUTPUTS</span></span>

### <span data-ttu-id="2a9e0-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2a9e0-139">System.Boolean</span></span>

## <span data-ttu-id="2a9e0-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2a9e0-140">NOTES</span></span>

<span data-ttu-id="2a9e0-141">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="2a9e0-141">ALIASES</span></span>

## <span data-ttu-id="2a9e0-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2a9e0-142">RELATED LINKS</span></span>

