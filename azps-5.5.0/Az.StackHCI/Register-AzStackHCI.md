---
external help file: Az.StackHCI-help.xml
Module Name: Az.StackHCI
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackhci/register-azstackhci
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Register-AzStackHCI.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Register-AzStackHCI.md
ms.openlocfilehash: a96ca28b750628eef1b0395e5867bb7f7341fba0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100150442"
---
# <span data-ttu-id="ee71c-101">Register-AzStackHCI</span><span class="sxs-lookup"><span data-stu-id="ee71c-101">Register-AzStackHCI</span></span>

## <span data-ttu-id="ee71c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee71c-102">SYNOPSIS</span></span>
<span data-ttu-id="ee71c-103">Register-AzStackHCI létrehoz egy Microsoft.AzureStackHCI felhőerőforrást, amely a helyi fürtnek megfelelő, és regisztrálja a helyi fürtöt az Azure-zal.</span><span class="sxs-lookup"><span data-stu-id="ee71c-103">Register-AzStackHCI creates a Microsoft.AzureStackHCI cloud resource representing the on-premise cluster and registers the on-premise cluster with Azure.</span></span>

## <span data-ttu-id="ee71c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ee71c-104">SYNTAX</span></span>

```
Register-AzStackHCI [-SubscriptionId] <String> [[-Region] <String>] [[-ResourceName] <String>]
 [[-TenantId] <String>] [[-ResourceGroupName] <String>] [[-ArmAccessToken] <String>]
 [[-GraphAccessToken] <String>] [[-AccountId] <String>] [[-EnvironmentName] <String>]
 [[-ComputerName] <String>] [[-CertificateThumbprint] <String>] [-RepairRegistration]
 [-UseDeviceAuthentication] [[-Credential] <PSCredential>] [<CommonParameters>]
```

## <span data-ttu-id="ee71c-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ee71c-105">DESCRIPTION</span></span>
<span data-ttu-id="ee71c-106">Register-AzStackHCI létrehoz egy Microsoft.AzureStackHCI felhőbeli erőforrást, amely a helyi fürtnek megfelelő, és regisztrálja a helyi fürtöt az Azure-ral.</span><span class="sxs-lookup"><span data-stu-id="ee71c-106">Register-AzStackHCI creates a Microsoft.AzureStackHCI cloud resource representing the on-premise cluster and registers the on-premise cluster with Azure.</span></span>

## <span data-ttu-id="ee71c-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ee71c-107">EXAMPLES</span></span>

### <span data-ttu-id="ee71c-108">1. PÉLDA</span><span class="sxs-lookup"><span data-stu-id="ee71c-108">EXAMPLE 1</span></span>
```powershell
C:\PS\>Register-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" 
Result: Success
ResourceId: /subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster1-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster1
PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster1-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster1/overview
PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/980be58d-578c-4cff-b4cd-43e9c3a77826/isMSAApp/
```

<span data-ttu-id="ee71c-109">Invoking on one the cluster node.</span><span class="sxs-lookup"><span data-stu-id="ee71c-109">Invoking on one of the cluster node.</span></span>

### <span data-ttu-id="ee71c-110">2. PÉLDA</span><span class="sxs-lookup"><span data-stu-id="ee71c-110">EXAMPLE 2</span></span>
```powershell
C:\PS\>Register-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ComputerName ClusterNode1
Result: Success
ResourceId: /subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster2-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster2
PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster2-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster2/overview
PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/950be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/
```

<span data-ttu-id="ee71c-111">Invoking from the management node.</span><span class="sxs-lookup"><span data-stu-id="ee71c-111">Invoking from the management node.</span></span>

### <span data-ttu-id="ee71c-112">3. PÉLDA</span><span class="sxs-lookup"><span data-stu-id="ee71c-112">EXAMPLE 3</span></span>
```powershell
C:\PS\>Register-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ArmAccessToken etyer..ere= -GraphAccessToken acyee..rerrer -AccountId user1@corp1.com -Region westus -ResourceName DemoHCICluster3 -ResourceGroupName DemoHCIRG 
Result: PendingForAdminConsent
ResourceId: /subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCIRG/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster3
PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCIRG/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster3/overview
PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/980be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/
```

<span data-ttu-id="ee71c-113">Invoking from WAC.</span><span class="sxs-lookup"><span data-stu-id="ee71c-113">Invoking from WAC.</span></span>

### <span data-ttu-id="ee71c-114">4. PÉLDA</span><span class="sxs-lookup"><span data-stu-id="ee71c-114">EXAMPLE 4</span></span>
```powershell
C:\PS\>Register-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -Region westus -ResourceName HciCluster1 -TenantId "c31c0dbb-ce27-4c78-ad26-a5f717c14557" -ResourceGroupName HciClusterRG -ArmAccessToken eerrer..ere= -GraphAccessToken acee..rerrer -AccountId user1@corp1.com -EnvironmentName AzureCloud -ComputerName node1hci -Credential Get-Credential
Result: Success
ResourceId: /subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/HciClusterRG/providers/Microsoft.AzureStackHCI/clusters/HciCluster1
PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/HciClusterRG/providers/Microsoft.AzureStackHCI/clusters/HciCluster1/overview
PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/990be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/
```

<span data-ttu-id="ee71c-115">Invoking with all the parameters.</span><span class="sxs-lookup"><span data-stu-id="ee71c-115">Invoking with all the parameters.</span></span>

## <span data-ttu-id="ee71c-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ee71c-116">PARAMETERS</span></span>

### <span data-ttu-id="ee71c-117">-AccountId</span><span class="sxs-lookup"><span data-stu-id="ee71c-117">-AccountId</span></span>
<span data-ttu-id="ee71c-118">Megadja a ARM hozzáférési jogkivonatot.</span><span class="sxs-lookup"><span data-stu-id="ee71c-118">Specifies the ARM access token.</span></span>
<span data-ttu-id="ee71c-119">Ha ezt az ArmAccessToken és a GraphAccessToken mellett adja meg, azzal elkerüli az Azure interaktív bejelentkezését.</span><span class="sxs-lookup"><span data-stu-id="ee71c-119">Specifying this along with ArmAccessToken and GraphAccessToken will avoid Azure interactive logon.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee71c-120">-ArmAccessToken</span><span class="sxs-lookup"><span data-stu-id="ee71c-120">-ArmAccessToken</span></span>
<span data-ttu-id="ee71c-121">Megadja a ARM hozzáférési jogkivonatot.</span><span class="sxs-lookup"><span data-stu-id="ee71c-121">Specifies the ARM access token.</span></span>
<span data-ttu-id="ee71c-122">Ha ezt a GraphAccessToken és az AccountId érték mellett adja meg, azzal elkerüli az Azure interaktív bejelentkezést.</span><span class="sxs-lookup"><span data-stu-id="ee71c-122">Specifying this along with GraphAccessToken and AccountId will avoid Azure interactive logon.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee71c-123">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="ee71c-123">-CertificateThumbprint</span></span>
<span data-ttu-id="ee71c-124">Az összes csomóponton elérhető tanúsítvány thumbprint-ját adja meg.</span><span class="sxs-lookup"><span data-stu-id="ee71c-124">Specifies the thumbprint of the certificate available on all the nodes.</span></span> <span data-ttu-id="ee71c-125">A felhasználó felelős a tanúsítvány kezeléséért.</span><span class="sxs-lookup"><span data-stu-id="ee71c-125">User is responsible for managing the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee71c-126">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="ee71c-126">-ComputerName</span></span>
<span data-ttu-id="ee71c-127">Megadja a fürt nevét vagy egy olyan fürtcsomópontot a környezetében, amely regisztrálva van az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="ee71c-127">Specifies the cluster name or one of the cluster node in on-premise cluster that is being registered to Azure.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee71c-128">-Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="ee71c-128">-Credential</span></span>
<span data-ttu-id="ee71c-129">A Számítógépnév hitelesítő adatait adja meg.</span><span class="sxs-lookup"><span data-stu-id="ee71c-129">Specifies the credential for the ComputerName.</span></span>
<span data-ttu-id="ee71c-130">Az alapértelmezett érték az a felhasználó, aki végrehajtja a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="ee71c-130">Default is the current user executing the Cmdlet.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 12
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee71c-131">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="ee71c-131">-EnvironmentName</span></span>
<span data-ttu-id="ee71c-132">Az Azure-környezetet határozza meg.</span><span class="sxs-lookup"><span data-stu-id="ee71c-132">Specifies the Azure Environment.</span></span>
<span data-ttu-id="ee71c-133">Az alapértelmezett érték az AzureCloud.</span><span class="sxs-lookup"><span data-stu-id="ee71c-133">Default is AzureCloud.</span></span>
<span data-ttu-id="ee71c-134">Érvényes értékek: AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span><span class="sxs-lookup"><span data-stu-id="ee71c-134">Valid values are AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: $AzureCloud
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee71c-135">-GraphAccessToken</span><span class="sxs-lookup"><span data-stu-id="ee71c-135">-GraphAccessToken</span></span>
<span data-ttu-id="ee71c-136">A Graph-hozzáférési jogkivonatot adja meg.</span><span class="sxs-lookup"><span data-stu-id="ee71c-136">Specifies the Graph access token.</span></span>
<span data-ttu-id="ee71c-137">Ha ezt az ArmAccessToken és az AccountId érték mellett adja meg, azzal elkerüli az Azure interaktív bejelentkezést.</span><span class="sxs-lookup"><span data-stu-id="ee71c-137">Specifying this along with ArmAccessToken and AccountId will avoid Azure interactive logon.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee71c-138">-Régió</span><span class="sxs-lookup"><span data-stu-id="ee71c-138">-Region</span></span>
<span data-ttu-id="ee71c-139">Megadja az erőforrás létrehozásához használt régiót.</span><span class="sxs-lookup"><span data-stu-id="ee71c-139">Specifies the Region to create the resource.</span></span>
<span data-ttu-id="ee71c-140">Az alapértelmezett érték az EastUS.</span><span class="sxs-lookup"><span data-stu-id="ee71c-140">Default is EastUS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee71c-141">-RepairRegistration</span><span class="sxs-lookup"><span data-stu-id="ee71c-141">-RepairRegistration</span></span>
<span data-ttu-id="ee71c-142">Kijavíthatja az Azure Stack HCI-regisztrációját a felhőben.</span><span class="sxs-lookup"><span data-stu-id="ee71c-142">Repair the current Azure Stack HCI registration with the cloud.</span></span> <span data-ttu-id="ee71c-143">Ez a parancsmag törli a helyi tanúsítványokat a csoportosított csomópontokon és a távoli tanúsítványokat az Azure AD-alkalmazásban a felhőben, és mindkettőhöz új cseretanúsítványokat hoz létre.</span><span class="sxs-lookup"><span data-stu-id="ee71c-143">This cmdlet deletes the local certificates on the clustered nodes and the remote certificates in the Azure AD application in the cloud and generates new replacement certificates for both.</span></span> <span data-ttu-id="ee71c-144">Az erőforráscsoport, az erőforrás neve és más regisztrációs lehetőségek megőrzve maradnak.</span><span class="sxs-lookup"><span data-stu-id="ee71c-144">The resource group, resource name, and other registration choices are preserved.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee71c-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee71c-145">-ResourceGroupName</span></span>
<span data-ttu-id="ee71c-146">Az Azure Erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ee71c-146">Specifies the Azure Resource Group name.</span></span>
<span data-ttu-id="ee71c-147">Ha nincs megadva ,rg, akkor az erőforráscsoport \<LocalClusterName\> neve lesz használatos.</span><span class="sxs-lookup"><span data-stu-id="ee71c-147">If not specified \<LocalClusterName\>-rg will be used as resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee71c-148">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="ee71c-148">-ResourceName</span></span>
<span data-ttu-id="ee71c-149">Az Azure-ban létrehozott erőforrás erőforrásnevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ee71c-149">Specifies the resource name of the resource created in Azure.</span></span>
<span data-ttu-id="ee71c-150">Ha nincs megadva, akkor a fürt neve a megadott időpontban történik.</span><span class="sxs-lookup"><span data-stu-id="ee71c-150">If not specified, on-premise cluster name is used.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee71c-151">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ee71c-151">-SubscriptionId</span></span>
<span data-ttu-id="ee71c-152">Megadja az erőforrás létrehozásához szükséges Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="ee71c-152">Specifies the Azure Subscription to create the resource.</span></span>
<span data-ttu-id="ee71c-153">Ez az egyetlen kötelező paraméter.</span><span class="sxs-lookup"><span data-stu-id="ee71c-153">This is the only Mandatory parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee71c-154">-TenantId</span><span class="sxs-lookup"><span data-stu-id="ee71c-154">-TenantId</span></span>
<span data-ttu-id="ee71c-155">Az Azure TenantId tulajdonságot adja meg.</span><span class="sxs-lookup"><span data-stu-id="ee71c-155">Specifies the Azure TenantId.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee71c-156">-UseDeviceAuthentication</span><span class="sxs-lookup"><span data-stu-id="ee71c-156">-UseDeviceAuthentication</span></span>
<span data-ttu-id="ee71c-157">Interaktív böngészőablak helyett használjon eszközkód-hitelesítést.</span><span class="sxs-lookup"><span data-stu-id="ee71c-157">Use device code authentication instead of an interactive browser prompt.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee71c-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee71c-158">CommonParameters</span></span>
<span data-ttu-id="ee71c-159">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee71c-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee71c-160">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ee71c-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee71c-161">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ee71c-161">INPUTS</span></span>

## <span data-ttu-id="ee71c-162">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ee71c-162">OUTPUTS</span></span>

### <span data-ttu-id="ee71c-163">PSCustomObject.</span><span class="sxs-lookup"><span data-stu-id="ee71c-163">PSCustomObject.</span></span> <span data-ttu-id="ee71c-164">A PSCustomObject tulajdonságot követő tulajdonságokat adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="ee71c-164">Returns following Properties in PSCustomObject</span></span>
### <span data-ttu-id="ee71c-165">Eredmény: Sikeres vagy sikertelen, illetve Függőben LévőForAdminConsent vagy Visszavonva.</span><span class="sxs-lookup"><span data-stu-id="ee71c-165">Result: Success or Failed or PendingForAdminConsent or Cancelled.</span></span>
### <span data-ttu-id="ee71c-166">ResourceId: Az Azure-ban létrehozott erőforrás erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="ee71c-166">ResourceId: Resource ID of the resource created in Azure.</span></span>
### <span data-ttu-id="ee71c-167">PortalResourceURL: Azure Portal Resource URL.</span><span class="sxs-lookup"><span data-stu-id="ee71c-167">PortalResourceURL: Azure Portal Resource URL.</span></span>
### <span data-ttu-id="ee71c-168">PortalAADAppPermissionsURL: Az Azure Portal AAD-alkalmazások engedélyeinek lapja.</span><span class="sxs-lookup"><span data-stu-id="ee71c-168">PortalAADAppPermissionsURL: Azure Portal URL for AAD App permissions page.</span></span>
## <span data-ttu-id="ee71c-169">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ee71c-169">NOTES</span></span>

## <span data-ttu-id="ee71c-170">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ee71c-170">RELATED LINKS</span></span>
