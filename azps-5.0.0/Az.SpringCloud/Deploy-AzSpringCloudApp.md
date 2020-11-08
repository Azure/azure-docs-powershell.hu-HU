---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.SpringCloud/deploy-azSpringCloudapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Deploy-AzSpringCloudApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Deploy-AzSpringCloudApp.md
ms.openlocfilehash: c6a7381c993b52995ab39a60fde54900092a5915
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185245"
---
# <span data-ttu-id="406af-101">Deploy-AzSpringCloudApp</span><span class="sxs-lookup"><span data-stu-id="406af-101">Deploy-AzSpringCloudApp</span></span>

## <span data-ttu-id="406af-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="406af-102">SYNOPSIS</span></span>
<span data-ttu-id="406af-103">Telepítse a beépített jar-ot a szolgáltatásba.</span><span class="sxs-lookup"><span data-stu-id="406af-103">Deploy the built jar to service.</span></span>

## <span data-ttu-id="406af-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="406af-104">SYNTAX</span></span>

```
Deploy-AzSpringCloudApp -JarPath <String> -Name <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="406af-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="406af-105">DESCRIPTION</span></span>
<span data-ttu-id="406af-106">Telepítse a beépített jar-ot a szolgáltatásba.</span><span class="sxs-lookup"><span data-stu-id="406af-106">Deploy the built jar to service.</span></span>

## <span data-ttu-id="406af-107">Példák</span><span class="sxs-lookup"><span data-stu-id="406af-107">EXAMPLES</span></span>

### <span data-ttu-id="406af-108">1. példa: telepítse a helyi lefordított jar szolgáltatást név szerint.</span><span class="sxs-lookup"><span data-stu-id="406af-108">Example 1: Deploy local compiled jar to service by name.</span></span>
```powershell
PS C:\> Deploy-AzSpringCloudApp -ResourceGroupName 'spring-cloud-rg' -ServiceName 'spring-cloud-service' -AppName 'gateway' -JarPath '/home/user/piggymetrics/gateway/target/gateway.jar'

[1/3] Requesting for upload URL
[2/3] Uploading package to blob
[3/3] Updating deployment in app account-service (this operation can take a while to complete)
Name Type
---- ----
prod Microsoft.AppPlatform/Spring/apps/deployments
```

<span data-ttu-id="406af-109">Telepítse a helyi lefordított jar szolgáltatást név szerint.</span><span class="sxs-lookup"><span data-stu-id="406af-109">Deploy local compiled jar to service by name.</span></span>

## <span data-ttu-id="406af-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="406af-110">PARAMETERS</span></span>

### <span data-ttu-id="406af-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="406af-111">-AsJob</span></span>
<span data-ttu-id="406af-112">A parancs futtatása munkaként</span><span class="sxs-lookup"><span data-stu-id="406af-112">Run the command as a job</span></span>

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

### <span data-ttu-id="406af-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="406af-113">-DefaultProfile</span></span>
<span data-ttu-id="406af-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="406af-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="406af-115">-JarPath</span><span class="sxs-lookup"><span data-stu-id="406af-115">-JarPath</span></span>
<span data-ttu-id="406af-116">A jar elérési útjának deploied kell lennie.</span><span class="sxs-lookup"><span data-stu-id="406af-116">The path of the jar need to be deploied.</span></span>

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

### <span data-ttu-id="406af-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="406af-117">-Name</span></span>
<span data-ttu-id="406af-118">Az App-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="406af-118">The name of the App resource.</span></span>

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

### <span data-ttu-id="406af-119">-Várva</span><span class="sxs-lookup"><span data-stu-id="406af-119">-NoWait</span></span>
<span data-ttu-id="406af-120">A parancs aszinkron futtatása</span><span class="sxs-lookup"><span data-stu-id="406af-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="406af-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="406af-121">-ResourceGroupName</span></span>
<span data-ttu-id="406af-122">Az erőforrást tartalmazó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="406af-122">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="406af-123">Ezt az értéket az Azure Resource Manager API-ból vagy a portálról kaphatja meg.</span><span class="sxs-lookup"><span data-stu-id="406af-123">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="406af-124">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="406af-124">-ServiceName</span></span>
<span data-ttu-id="406af-125">A szolgáltatás erőforrásának neve.</span><span class="sxs-lookup"><span data-stu-id="406af-125">The name of the Service resource.</span></span>

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

### <span data-ttu-id="406af-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="406af-126">-SubscriptionId</span></span>
<span data-ttu-id="406af-127">Megkapja az előfizetés AZONOSÍTÓját, amely egyedileg azonosítja a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="406af-127">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="406af-128">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="406af-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="406af-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="406af-129">-Confirm</span></span>
<span data-ttu-id="406af-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="406af-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="406af-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="406af-131">-WhatIf</span></span>
<span data-ttu-id="406af-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="406af-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="406af-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="406af-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="406af-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="406af-134">CommonParameters</span></span>
<span data-ttu-id="406af-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="406af-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="406af-136">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="406af-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="406af-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="406af-137">INPUTS</span></span>

## <span data-ttu-id="406af-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="406af-138">OUTPUTS</span></span>

### <span data-ttu-id="406af-139">Microsoft. Azure. PowerShell. parancsmagok. SpringCloud. modellek. Api20200701. IAppResource</span><span class="sxs-lookup"><span data-stu-id="406af-139">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IAppResource</span></span>

## <span data-ttu-id="406af-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="406af-140">NOTES</span></span>

<span data-ttu-id="406af-141">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="406af-141">ALIASES</span></span>

## <span data-ttu-id="406af-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="406af-142">RELATED LINKS</span></span>

