---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.SpringCloud/deploy-azSpringCloudapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Deploy-AzSpringCloudApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Deploy-AzSpringCloudApp.md
ms.openlocfilehash: c6a7381c993b52995ab39a60fde54900092a5915
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479505"
---
# <span data-ttu-id="aefa7-101">Deploy-AzSpringCloudApp</span><span class="sxs-lookup"><span data-stu-id="aefa7-101">Deploy-AzSpringCloudApp</span></span>

## <span data-ttu-id="aefa7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aefa7-102">SYNOPSIS</span></span>
<span data-ttu-id="aefa7-103">Telepítse a beépített üveget szervizbe.</span><span class="sxs-lookup"><span data-stu-id="aefa7-103">Deploy the built jar to service.</span></span>

## <span data-ttu-id="aefa7-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="aefa7-104">SYNTAX</span></span>

```
Deploy-AzSpringCloudApp -JarPath <String> -Name <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="aefa7-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="aefa7-105">DESCRIPTION</span></span>
<span data-ttu-id="aefa7-106">Telepítse a beépített üveget szervizbe.</span><span class="sxs-lookup"><span data-stu-id="aefa7-106">Deploy the built jar to service.</span></span>

## <span data-ttu-id="aefa7-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="aefa7-107">EXAMPLES</span></span>

### <span data-ttu-id="aefa7-108">1. példa: Telepítse a helyi lefordított üveget a szolgáltatáshoz név szerint.</span><span class="sxs-lookup"><span data-stu-id="aefa7-108">Example 1: Deploy local compiled jar to service by name.</span></span>
```powershell
PS C:\> Deploy-AzSpringCloudApp -ResourceGroupName 'spring-cloud-rg' -ServiceName 'spring-cloud-service' -AppName 'gateway' -JarPath '/home/user/piggymetrics/gateway/target/gateway.jar'

[1/3] Requesting for upload URL
[2/3] Uploading package to blob
[3/3] Updating deployment in app account-service (this operation can take a while to complete)
Name Type
---- ----
prod Microsoft.AppPlatform/Spring/apps/deployments
```

<span data-ttu-id="aefa7-109">Telepítse a helyi lefordított üveget a szolgáltatáshoz név szerint.</span><span class="sxs-lookup"><span data-stu-id="aefa7-109">Deploy local compiled jar to service by name.</span></span>

## <span data-ttu-id="aefa7-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aefa7-110">PARAMETERS</span></span>

### <span data-ttu-id="aefa7-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="aefa7-111">-AsJob</span></span>
<span data-ttu-id="aefa7-112">A parancs futtatása feladatként</span><span class="sxs-lookup"><span data-stu-id="aefa7-112">Run the command as a job</span></span>

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

### <span data-ttu-id="aefa7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aefa7-113">-DefaultProfile</span></span>
<span data-ttu-id="aefa7-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="aefa7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aefa7-115">-JarPath</span><span class="sxs-lookup"><span data-stu-id="aefa7-115">-JarPath</span></span>
<span data-ttu-id="aefa7-116">Az üveg útvonalát fel kell szabadodni.</span><span class="sxs-lookup"><span data-stu-id="aefa7-116">The path of the jar need to be deploied.</span></span>

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

### <span data-ttu-id="aefa7-117">-Name</span><span class="sxs-lookup"><span data-stu-id="aefa7-117">-Name</span></span>
<span data-ttu-id="aefa7-118">Az alkalmazáserőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="aefa7-118">The name of the App resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AppName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aefa7-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="aefa7-119">-NoWait</span></span>
<span data-ttu-id="aefa7-120">A parancs futtatása aszinkron módon</span><span class="sxs-lookup"><span data-stu-id="aefa7-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="aefa7-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aefa7-121">-ResourceGroupName</span></span>
<span data-ttu-id="aefa7-122">Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="aefa7-122">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="aefa7-123">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról szerezheti be.</span><span class="sxs-lookup"><span data-stu-id="aefa7-123">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="aefa7-124">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="aefa7-124">-ServiceName</span></span>
<span data-ttu-id="aefa7-125">A Szolgáltatás erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="aefa7-125">The name of the Service resource.</span></span>

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

### <span data-ttu-id="aefa7-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="aefa7-126">-SubscriptionId</span></span>
<span data-ttu-id="aefa7-127">Olyan előfizetésazonosítót kap, amely egyedileg azonosítja a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="aefa7-127">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="aefa7-128">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="aefa7-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="aefa7-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aefa7-129">-Confirm</span></span>
<span data-ttu-id="aefa7-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="aefa7-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aefa7-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aefa7-131">-WhatIf</span></span>
<span data-ttu-id="aefa7-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="aefa7-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aefa7-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="aefa7-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aefa7-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aefa7-134">CommonParameters</span></span>
<span data-ttu-id="aefa7-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aefa7-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aefa7-136">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="aefa7-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aefa7-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="aefa7-137">INPUTS</span></span>

## <span data-ttu-id="aefa7-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="aefa7-138">OUTPUTS</span></span>

### <span data-ttu-id="aefa7-139">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IAppResource</span><span class="sxs-lookup"><span data-stu-id="aefa7-139">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IAppResource</span></span>

## <span data-ttu-id="aefa7-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="aefa7-140">NOTES</span></span>

<span data-ttu-id="aefa7-141">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="aefa7-141">ALIASES</span></span>

## <span data-ttu-id="aefa7-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="aefa7-142">RELATED LINKS</span></span>

