---
external help file: Az.StackHCI-help.xml
Module Name: Az.StackHCI
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackhci/unregister-azstackhci
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Unregister-AzStackHCI.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Unregister-AzStackHCI.md
ms.openlocfilehash: cc887fb8e41fd9464914144e7cbed5a332948228
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187192"
---
# <span data-ttu-id="fb2a9-101">Unregister-AzStackHCI</span><span class="sxs-lookup"><span data-stu-id="fb2a9-101">Unregister-AzStackHCI</span></span>

## <span data-ttu-id="fb2a9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fb2a9-102">SYNOPSIS</span></span>
<span data-ttu-id="fb2a9-103">Unregister-AzStackHCI törli a helyszíni fürtöt képviselő Microsoft. AzureStackHCI felhőalapú erőforrást, és a helyszíni fürtöt eltávolítja az Azure rendszerből.</span><span class="sxs-lookup"><span data-stu-id="fb2a9-103">Unregister-AzStackHCI deletes the Microsoft.AzureStackHCI cloud resource representing the on-premise cluster and unregisters the on-premise cluster with Azure.</span></span>
<span data-ttu-id="fb2a9-104">A fürtben rendelkezésre álló regisztrált adatok a fürt regisztrációjának törlésére szolgálnak, ha nincs paraméter átadva.</span><span class="sxs-lookup"><span data-stu-id="fb2a9-104">The registered information available on the cluster is used to unregister the cluster if no parameters are passed.</span></span>

## <span data-ttu-id="fb2a9-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fb2a9-105">SYNTAX</span></span>

```
Unregister-AzStackHCI [[-SubscriptionId] <String>] [[-ResourceName] <String>] [[-TenantId] <String>]
 [[-ResourceGroupName] <String>] [[-ArmAccessToken] <String>] [[-GraphAccessToken] <String>]
 [[-AccountId] <String>] [[-EnvironmentName] <String>] [[-ComputerName] <String>]
 [[-Credential] <PSCredential>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb2a9-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="fb2a9-106">DESCRIPTION</span></span>
<span data-ttu-id="fb2a9-107">Unregister-AzStackHCI törli a helyszíni fürtöt képviselő Microsoft. AzureStackHCI felhőalapú erőforrást, és a helyszíni fürtöt eltávolítja az Azure rendszerből.</span><span class="sxs-lookup"><span data-stu-id="fb2a9-107">Unregister-AzStackHCI deletes the Microsoft.AzureStackHCI cloud resource representing the on-premise cluster and unregisters the on-premise cluster with Azure.</span></span>
<span data-ttu-id="fb2a9-108">A fürtben rendelkezésre álló regisztrált adatok a fürt regisztrációjának törlésére szolgálnak, ha nincs paraméter átadva.</span><span class="sxs-lookup"><span data-stu-id="fb2a9-108">The registered information available on the cluster is used to unregister the cluster if no parameters are passed.</span></span>

## <span data-ttu-id="fb2a9-109">Példák</span><span class="sxs-lookup"><span data-stu-id="fb2a9-109">EXAMPLES</span></span>

### <span data-ttu-id="fb2a9-110">PÉLDA 1</span><span class="sxs-lookup"><span data-stu-id="fb2a9-110">EXAMPLE 1</span></span>
```
Invoking on one of the cluster node
```

<span data-ttu-id="fb2a9-111">C:\PS \> unregister-AzStackHCI eredmény: siker</span><span class="sxs-lookup"><span data-stu-id="fb2a9-111">C:\PS\>Unregister-AzStackHCI Result: Success</span></span>

### <span data-ttu-id="fb2a9-112">2. PÉLDA</span><span class="sxs-lookup"><span data-stu-id="fb2a9-112">EXAMPLE 2</span></span>
```
Invoking from the management node
```

<span data-ttu-id="fb2a9-113">C:\PS \> unregister-AzStackHCI-számítógép_neve ClusterNode1 result: Success (siker)</span><span class="sxs-lookup"><span data-stu-id="fb2a9-113">C:\PS\>Unregister-AzStackHCI -ComputerName ClusterNode1 Result: Success</span></span>

### <span data-ttu-id="fb2a9-114">3. PÉLDA</span><span class="sxs-lookup"><span data-stu-id="fb2a9-114">EXAMPLE 3</span></span>
```
Invoking from WAC
```

<span data-ttu-id="fb2a9-115">C:\PS \> unregister-AzStackHCI-SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd"-ArmAccessToken etyer.. ere =-GraphAccessToken acyee.. rerrer-AccountId user1@corp1.com -resourcename DemoHCICluster3-ResourceGroupName DemoHCIRG – megerősítés: $false eredmény: siker</span><span class="sxs-lookup"><span data-stu-id="fb2a9-115">C:\PS\>Unregister-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ArmAccessToken etyer..ere= -GraphAccessToken acyee..rerrer -AccountId user1@corp1.com -ResourceName DemoHCICluster3 -ResourceGroupName DemoHCIRG -Confirm:$False Result: Success</span></span>

### <span data-ttu-id="fb2a9-116">4. PÉLDA</span><span class="sxs-lookup"><span data-stu-id="fb2a9-116">EXAMPLE 4</span></span>
```
Invoking with all the parameters
```

<span data-ttu-id="fb2a9-117">C:\PS \> unregister-AzStackHCI-SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd"-resourcename HciCluster1-bérlői azonosító megkeresése "c31c0dbb-ce27-4c78-ad26-a5f717c14557"-ResourceGroupName-HciClusterRG-ArmAccessToken eerrer.. ere =-GraphAccessToken acee.. rerrer-AccountId user1@corp1.com -EnvironmentName AzureCloud-számítógép_neve node1hci-hitelesítő adatok Get-Credential eredmény: siker</span><span class="sxs-lookup"><span data-stu-id="fb2a9-117">C:\PS\>Unregister-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ResourceName HciCluster1 -TenantId "c31c0dbb-ce27-4c78-ad26-a5f717c14557" -ResourceGroupName HciClusterRG -ArmAccessToken eerrer..ere= -GraphAccessToken acee..rerrer -AccountId user1@corp1.com -EnvironmentName AzureCloud -ComputerName node1hci -Credential Get-Credential Result: Success</span></span>

## <span data-ttu-id="fb2a9-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fb2a9-118">PARAMETERS</span></span>

### <span data-ttu-id="fb2a9-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fb2a9-119">-SubscriptionId</span></span>
<span data-ttu-id="fb2a9-120">Az Azure-előfizetést adja meg az erőforrás létrehozásához</span><span class="sxs-lookup"><span data-stu-id="fb2a9-120">Specifies the Azure Subscription to create the resource</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb2a9-121">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="fb2a9-121">-ResourceName</span></span>
<span data-ttu-id="fb2a9-122">Az Azure-ban létrehozott erőforrás erőforrásának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fb2a9-122">Specifies the resource name of the resource created in Azure.</span></span>
<span data-ttu-id="fb2a9-123">Ha nem adja meg, akkor a helyszíni fürt nevét használja a rendszer.</span><span class="sxs-lookup"><span data-stu-id="fb2a9-123">If not specified, on-premise cluster name is used.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb2a9-124">-Bérlői azonosító megkeresése</span><span class="sxs-lookup"><span data-stu-id="fb2a9-124">-TenantId</span></span>
<span data-ttu-id="fb2a9-125">Az Azure bérlői azonosító megkeresése adja meg.</span><span class="sxs-lookup"><span data-stu-id="fb2a9-125">Specifies the Azure TenantId.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb2a9-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb2a9-126">-ResourceGroupName</span></span>
<span data-ttu-id="fb2a9-127">Az Azure Resource Group nevet adja meg.</span><span class="sxs-lookup"><span data-stu-id="fb2a9-127">Specifies the Azure Resource Group name.</span></span>
<span data-ttu-id="fb2a9-128">Ha nem adja meg \<LocalClusterName\> a-RG nevet, a program erőforrás-csoportként használja.</span><span class="sxs-lookup"><span data-stu-id="fb2a9-128">If not specified \<LocalClusterName\>-rg will be used as resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb2a9-129">-ArmAccessToken</span><span class="sxs-lookup"><span data-stu-id="fb2a9-129">-ArmAccessToken</span></span>
<span data-ttu-id="fb2a9-130">A ARM hozzáférési tokent adja meg.</span><span class="sxs-lookup"><span data-stu-id="fb2a9-130">Specifies the ARM access token.</span></span>
<span data-ttu-id="fb2a9-131">A GraphAccessToken és a AccountId együtt az Azure interaktív bejelentkezést is el kell kerülnie.</span><span class="sxs-lookup"><span data-stu-id="fb2a9-131">Specifying this along with GraphAccessToken and AccountId will avoid Azure interactive logon.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb2a9-132">-GraphAccessToken</span><span class="sxs-lookup"><span data-stu-id="fb2a9-132">-GraphAccessToken</span></span>
<span data-ttu-id="fb2a9-133">A Graph Access-tokent adja meg.</span><span class="sxs-lookup"><span data-stu-id="fb2a9-133">Specifies the Graph access token.</span></span>
<span data-ttu-id="fb2a9-134">A ArmAccessToken és a AccountId együtt az Azure interaktív bejelentkezést is el kell kerülnie.</span><span class="sxs-lookup"><span data-stu-id="fb2a9-134">Specifying this along with ArmAccessToken and AccountId will avoid Azure interactive logon.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb2a9-135">-AccountId</span><span class="sxs-lookup"><span data-stu-id="fb2a9-135">-AccountId</span></span>
<span data-ttu-id="fb2a9-136">A ARM hozzáférési tokent adja meg.</span><span class="sxs-lookup"><span data-stu-id="fb2a9-136">Specifies the ARM access token.</span></span>
<span data-ttu-id="fb2a9-137">A ArmAccessToken és a GraphAccessToken együtt az Azure interaktív bejelentkezést is el kell kerülnie.</span><span class="sxs-lookup"><span data-stu-id="fb2a9-137">Specifying this along with ArmAccessToken and GraphAccessToken will avoid Azure interactive logon.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb2a9-138">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="fb2a9-138">-EnvironmentName</span></span>
<span data-ttu-id="fb2a9-139">Az Azure-környezetet adja meg.</span><span class="sxs-lookup"><span data-stu-id="fb2a9-139">Specifies the Azure Environment.</span></span>
<span data-ttu-id="fb2a9-140">Az alapértelmezett érték a AzureCloud.</span><span class="sxs-lookup"><span data-stu-id="fb2a9-140">Default is AzureCloud.</span></span>
<span data-ttu-id="fb2a9-141">Az érvényes értékek a következők AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span><span class="sxs-lookup"><span data-stu-id="fb2a9-141">Valid values are AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: $AzureCloud
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb2a9-142">-Számítógépnév</span><span class="sxs-lookup"><span data-stu-id="fb2a9-142">-ComputerName</span></span>
<span data-ttu-id="fb2a9-143">A helyszíni fürtökben az Azure rendszerhez regisztrált fürtcsomópont egyik csomópontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="fb2a9-143">Specifies one of the cluster node in on-premise cluster that is being registered to Azure.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb2a9-144">-Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="fb2a9-144">-Credential</span></span>
<span data-ttu-id="fb2a9-145">A számítógépnév hitelesítő adatait adja meg.</span><span class="sxs-lookup"><span data-stu-id="fb2a9-145">Specifies the credential for the ComputerName.</span></span>
<span data-ttu-id="fb2a9-146">Az alapértelmezett beállítás a parancsmagot végrehajtó jelenlegi felhasználó.</span><span class="sxs-lookup"><span data-stu-id="fb2a9-146">Default is the current user executing the Cmdlet.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb2a9-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb2a9-147">-WhatIf</span></span>
<span data-ttu-id="fb2a9-148">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="fb2a9-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb2a9-149">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fb2a9-149">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb2a9-150">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="fb2a9-150">-Confirm</span></span>
<span data-ttu-id="fb2a9-151">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="fb2a9-151">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb2a9-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb2a9-152">CommonParameters</span></span>
<span data-ttu-id="fb2a9-153">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fb2a9-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb2a9-154">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="fb2a9-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb2a9-155">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fb2a9-155">INPUTS</span></span>

## <span data-ttu-id="fb2a9-156">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fb2a9-156">OUTPUTS</span></span>

### <span data-ttu-id="fb2a9-157">PSCustomObject.</span><span class="sxs-lookup"><span data-stu-id="fb2a9-157">PSCustomObject.</span></span> <span data-ttu-id="fb2a9-158">Az PSCustomObject az alábbi tulajdonságokat számítja ki.</span><span class="sxs-lookup"><span data-stu-id="fb2a9-158">Returns following Properties in PSCustomObject</span></span>
### <span data-ttu-id="fb2a9-159">Eredmény: sikeres vagy sikertelen vagy lemondott.</span><span class="sxs-lookup"><span data-stu-id="fb2a9-159">Result: Success or Failed or Cancelled.</span></span>
## <span data-ttu-id="fb2a9-160">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fb2a9-160">NOTES</span></span>

## <span data-ttu-id="fb2a9-161">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fb2a9-161">RELATED LINKS</span></span>
