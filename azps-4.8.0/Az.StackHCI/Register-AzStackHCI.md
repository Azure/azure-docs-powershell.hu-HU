---
external help file: Az.StackHCI-help.xml
Module Name: Az.StackHCI
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackhci/register-azstackhci
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Register-AzStackHCI.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Register-AzStackHCI.md
ms.openlocfilehash: c09c4b4c8d71d90bbbac0771c75ea3ea51ee05dc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183191"
---
# <span data-ttu-id="b1afa-101">Register-AzStackHCI</span><span class="sxs-lookup"><span data-stu-id="b1afa-101">Register-AzStackHCI</span></span>

## <span data-ttu-id="b1afa-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b1afa-102">SYNOPSIS</span></span>
<span data-ttu-id="b1afa-103">A Register-AzStackHCI létrehoz egy Microsoft. AzureStackHCI felhőalapú erőforrást, amely a helyszíni fürtöt képviseli, és a helyszíni fürtöt regisztrálja az Azuretal.</span><span class="sxs-lookup"><span data-stu-id="b1afa-103">Register-AzStackHCI creates a Microsoft.AzureStackHCI cloud resource representing the on-premise cluster and registers the on-premise cluster with Azure.</span></span>

## <span data-ttu-id="b1afa-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b1afa-104">SYNTAX</span></span>

```
Register-AzStackHCI [-SubscriptionId] <String> [[-Region] <String>] [[-ResourceName] <String>]
 [[-TenantId] <String>] [[-ResourceGroupName] <String>] [[-ArmAccessToken] <String>]
 [[-GraphAccessToken] <String>] [[-AccountId] <String>] [[-EnvironmentName] <String>]
 [[-ComputerName] <String>] [[-Credential] <PSCredential>] [<CommonParameters>]
```

## <span data-ttu-id="b1afa-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b1afa-105">DESCRIPTION</span></span>
<span data-ttu-id="b1afa-106">A Register-AzStackHCI létrehoz egy Microsoft. AzureStackHCI felhőalapú erőforrást, amely a helyszíni fürtöt képviseli, és a helyszíni fürtöt regisztrálja az Azuretal.</span><span class="sxs-lookup"><span data-stu-id="b1afa-106">Register-AzStackHCI creates a Microsoft.AzureStackHCI cloud resource representing the on-premise cluster and registers the on-premise cluster with Azure.</span></span>

## <span data-ttu-id="b1afa-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b1afa-107">EXAMPLES</span></span>

### <span data-ttu-id="b1afa-108">PÉLDA 1</span><span class="sxs-lookup"><span data-stu-id="b1afa-108">EXAMPLE 1</span></span>
```
Invoking on one of the cluster node.
```

<span data-ttu-id="b1afa-109">C:\PS \> Register-AzStackHCI-SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" result: Success ResourceId:/Subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster1-RG/Providers/Microsoft.AzureStackHCI/Clusters/DemoHCICluster1 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster1-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster1/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/980be58d-578c-4cff-b4cd-43e9c3a77826/isMSAApp/</span><span class="sxs-lookup"><span data-stu-id="b1afa-109">C:\PS\>Register-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" Result: Success ResourceId: /subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster1-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster1 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster1-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster1/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/980be58d-578c-4cff-b4cd-43e9c3a77826/isMSAApp/</span></span>

### <span data-ttu-id="b1afa-110">2. PÉLDA</span><span class="sxs-lookup"><span data-stu-id="b1afa-110">EXAMPLE 2</span></span>
```
Invoking from the management node
```

<span data-ttu-id="b1afa-111">C:\PS \> Register-AzStackHCI-SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd"-számítógép_neve ClusterNode1 result: Success ResourceId:/Subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster2-RG/Providers/Microsoft.AzureStackHCI/Clusters/DemoHCICluster2 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster2-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster2/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/950be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/</span><span class="sxs-lookup"><span data-stu-id="b1afa-111">C:\PS\>Register-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ComputerName ClusterNode1 Result: Success ResourceId: /subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster2-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster2 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster2-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster2/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/950be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/</span></span>

### <span data-ttu-id="b1afa-112">3. PÉLDA</span><span class="sxs-lookup"><span data-stu-id="b1afa-112">EXAMPLE 3</span></span>
```
Invoking from WAC
```

<span data-ttu-id="b1afa-113">C:\PS \> Register-AzStackHCI-SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd"-ArmAccessToken etyer.. ere =-GraphAccessToken acyee.. rerrer-AccountId user1@corp1.com -region westus-resourcename DemoHCICluster3-ResourceGroupName DemoHCIRG result: PendingForAdminConsent ResourceId:/Subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCIRG/Providers/Microsoft.AzureStackHCI/Clusters/DemoHCICluster3 https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCIRG/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster3/overview PortalResourceURL: PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/980be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/</span><span class="sxs-lookup"><span data-stu-id="b1afa-113">C:\PS\>Register-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ArmAccessToken etyer..ere= -GraphAccessToken acyee..rerrer -AccountId user1@corp1.com -Region westus -ResourceName DemoHCICluster3 -ResourceGroupName DemoHCIRG Result: PendingForAdminConsent ResourceId: /subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCIRG/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster3 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCIRG/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster3/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/980be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/</span></span>

### <span data-ttu-id="b1afa-114">4. PÉLDA</span><span class="sxs-lookup"><span data-stu-id="b1afa-114">EXAMPLE 4</span></span>
```
Invoking with all the parameters
```

<span data-ttu-id="b1afa-115">C:\PS \> Register-AzStackHCI-SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd"-Region westus-resourcename HciCluster1-bérlői azonosító megkeresése "c31c0dbb-ce27-4c78-ad26-a5f717c14557"-ResourceGroupName HciClusterRG-ArmAccessToken eerrer.. ere =-GraphAccessToken acee.. rerrer-AccountId user1@corp1.com -EnvironmentName AzureCloud-számítógépnév node1hci-hitelesítő Get-Credential eredmény: Success ResourceId:/Subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/HciClusterRG/Providers/Microsoft.AzureStackHCI/Clusters/HciCluster1 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/HciClusterRG/providers/Microsoft.AzureStackHCI/clusters/HciCluster1/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/990be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/</span><span class="sxs-lookup"><span data-stu-id="b1afa-115">C:\PS\>Register-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -Region westus -ResourceName HciCluster1 -TenantId "c31c0dbb-ce27-4c78-ad26-a5f717c14557" -ResourceGroupName HciClusterRG -ArmAccessToken eerrer..ere= -GraphAccessToken acee..rerrer -AccountId user1@corp1.com -EnvironmentName AzureCloud -ComputerName node1hci -Credential Get-Credential Result: Success ResourceId: /subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/HciClusterRG/providers/Microsoft.AzureStackHCI/clusters/HciCluster1 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/HciClusterRG/providers/Microsoft.AzureStackHCI/clusters/HciCluster1/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/990be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/</span></span>

## <span data-ttu-id="b1afa-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b1afa-116">PARAMETERS</span></span>

### <span data-ttu-id="b1afa-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b1afa-117">-SubscriptionId</span></span>
<span data-ttu-id="b1afa-118">Az Azure-előfizetést adja meg az erőforrás létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="b1afa-118">Specifies the Azure Subscription to create the resource.</span></span>
<span data-ttu-id="b1afa-119">Ez az egyetlen kötelező paraméter.</span><span class="sxs-lookup"><span data-stu-id="b1afa-119">This is the only Mandatory parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1afa-120">-Region (régió)</span><span class="sxs-lookup"><span data-stu-id="b1afa-120">-Region</span></span>
<span data-ttu-id="b1afa-121">Az erőforrást létrehozó régiót adja meg.</span><span class="sxs-lookup"><span data-stu-id="b1afa-121">Specifies the Region to create the resource.</span></span>
<span data-ttu-id="b1afa-122">Az alapértelmezett érték a EastUS.</span><span class="sxs-lookup"><span data-stu-id="b1afa-122">Default is EastUS.</span></span>

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

### <span data-ttu-id="b1afa-123">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="b1afa-123">-ResourceName</span></span>
<span data-ttu-id="b1afa-124">Az Azure-ban létrehozott erőforrás erőforrásának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b1afa-124">Specifies the resource name of the resource created in Azure.</span></span>
<span data-ttu-id="b1afa-125">Ha nem adja meg, akkor a helyszíni fürt nevét használja a rendszer.</span><span class="sxs-lookup"><span data-stu-id="b1afa-125">If not specified, on-premise cluster name is used.</span></span>

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

### <span data-ttu-id="b1afa-126">-Bérlői azonosító megkeresése</span><span class="sxs-lookup"><span data-stu-id="b1afa-126">-TenantId</span></span>
<span data-ttu-id="b1afa-127">Az Azure bérlői azonosító megkeresése adja meg.</span><span class="sxs-lookup"><span data-stu-id="b1afa-127">Specifies the Azure TenantId.</span></span>

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

### <span data-ttu-id="b1afa-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1afa-128">-ResourceGroupName</span></span>
<span data-ttu-id="b1afa-129">Az Azure Resource Group nevet adja meg.</span><span class="sxs-lookup"><span data-stu-id="b1afa-129">Specifies the Azure Resource Group name.</span></span>
<span data-ttu-id="b1afa-130">Ha nem adja meg \<LocalClusterName\> a-RG nevet, a program erőforrás-csoportként használja.</span><span class="sxs-lookup"><span data-stu-id="b1afa-130">If not specified \<LocalClusterName\>-rg will be used as resource group name.</span></span>

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

### <span data-ttu-id="b1afa-131">-ArmAccessToken</span><span class="sxs-lookup"><span data-stu-id="b1afa-131">-ArmAccessToken</span></span>
<span data-ttu-id="b1afa-132">A ARM hozzáférési tokent adja meg.</span><span class="sxs-lookup"><span data-stu-id="b1afa-132">Specifies the ARM access token.</span></span>
<span data-ttu-id="b1afa-133">A GraphAccessToken és a AccountId együtt az Azure interaktív bejelentkezést is el kell kerülnie.</span><span class="sxs-lookup"><span data-stu-id="b1afa-133">Specifying this along with GraphAccessToken and AccountId will avoid Azure interactive logon.</span></span>

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

### <span data-ttu-id="b1afa-134">-GraphAccessToken</span><span class="sxs-lookup"><span data-stu-id="b1afa-134">-GraphAccessToken</span></span>
<span data-ttu-id="b1afa-135">A Graph Access-tokent adja meg.</span><span class="sxs-lookup"><span data-stu-id="b1afa-135">Specifies the Graph access token.</span></span>
<span data-ttu-id="b1afa-136">A ArmAccessToken és a AccountId együtt az Azure interaktív bejelentkezést is el kell kerülnie.</span><span class="sxs-lookup"><span data-stu-id="b1afa-136">Specifying this along with ArmAccessToken and AccountId will avoid Azure interactive logon.</span></span>

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

### <span data-ttu-id="b1afa-137">-AccountId</span><span class="sxs-lookup"><span data-stu-id="b1afa-137">-AccountId</span></span>
<span data-ttu-id="b1afa-138">A ARM hozzáférési tokent adja meg.</span><span class="sxs-lookup"><span data-stu-id="b1afa-138">Specifies the ARM access token.</span></span>
<span data-ttu-id="b1afa-139">A ArmAccessToken és a GraphAccessToken együtt az Azure interaktív bejelentkezést is el kell kerülnie.</span><span class="sxs-lookup"><span data-stu-id="b1afa-139">Specifying this along with ArmAccessToken and GraphAccessToken will avoid Azure interactive logon.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1afa-140">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="b1afa-140">-EnvironmentName</span></span>
<span data-ttu-id="b1afa-141">Az Azure-környezetet adja meg.</span><span class="sxs-lookup"><span data-stu-id="b1afa-141">Specifies the Azure Environment.</span></span>
<span data-ttu-id="b1afa-142">Az alapértelmezett érték a AzureCloud.</span><span class="sxs-lookup"><span data-stu-id="b1afa-142">Default is AzureCloud.</span></span>
<span data-ttu-id="b1afa-143">Az érvényes értékek a következők AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span><span class="sxs-lookup"><span data-stu-id="b1afa-143">Valid values are AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: $AzureCloud
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1afa-144">-Számítógépnév</span><span class="sxs-lookup"><span data-stu-id="b1afa-144">-ComputerName</span></span>
<span data-ttu-id="b1afa-145">A helyszíni fürtökben az Azure rendszerhez regisztrált fürt nevét vagy a fürtcsomópont egyik csomópontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="b1afa-145">Specifies the cluster name or one of the cluster node in on-premise cluster that is being registered to Azure.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1afa-146">-Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="b1afa-146">-Credential</span></span>
<span data-ttu-id="b1afa-147">A számítógépnév hitelesítő adatait adja meg.</span><span class="sxs-lookup"><span data-stu-id="b1afa-147">Specifies the credential for the ComputerName.</span></span>
<span data-ttu-id="b1afa-148">Az alapértelmezett beállítás a parancsmagot végrehajtó jelenlegi felhasználó.</span><span class="sxs-lookup"><span data-stu-id="b1afa-148">Default is the current user executing the Cmdlet.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1afa-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1afa-149">CommonParameters</span></span>
<span data-ttu-id="b1afa-150">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b1afa-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1afa-151">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b1afa-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1afa-152">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b1afa-152">INPUTS</span></span>

## <span data-ttu-id="b1afa-153">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b1afa-153">OUTPUTS</span></span>

### <span data-ttu-id="b1afa-154">PSCustomObject.</span><span class="sxs-lookup"><span data-stu-id="b1afa-154">PSCustomObject.</span></span> <span data-ttu-id="b1afa-155">Az PSCustomObject az alábbi tulajdonságokat számítja ki.</span><span class="sxs-lookup"><span data-stu-id="b1afa-155">Returns following Properties in PSCustomObject</span></span>
### <span data-ttu-id="b1afa-156">Eredmény: sikeres, sikertelen vagy PendingForAdminConsent vagy lemondott.</span><span class="sxs-lookup"><span data-stu-id="b1afa-156">Result: Success or Failed or PendingForAdminConsent or Cancelled.</span></span>
### <span data-ttu-id="b1afa-157">ResourceId: az Azure-ban létrehozott erőforrás erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="b1afa-157">ResourceId: Resource ID of the resource created in Azure.</span></span>
### <span data-ttu-id="b1afa-158">PortalResourceURL: Azure portál erőforrás-URL-címe.</span><span class="sxs-lookup"><span data-stu-id="b1afa-158">PortalResourceURL: Azure Portal Resource URL.</span></span>
### <span data-ttu-id="b1afa-159">PortalAADAppPermissionsURL: Azure portál URL-címe a AAD app engedélyeinek lapjáról.</span><span class="sxs-lookup"><span data-stu-id="b1afa-159">PortalAADAppPermissionsURL: Azure Portal URL for AAD App permissions page.</span></span>
## <span data-ttu-id="b1afa-160">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b1afa-160">NOTES</span></span>

## <span data-ttu-id="b1afa-161">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b1afa-161">RELATED LINKS</span></span>
