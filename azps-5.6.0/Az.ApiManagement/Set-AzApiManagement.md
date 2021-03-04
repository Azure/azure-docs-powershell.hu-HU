---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/set-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagement.md
ms.openlocfilehash: 3f1ab16dd6bf8dd264bdb4e4427d45197feace7b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101928402"
---
# <span data-ttu-id="e23e9-101">Set-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="e23e9-101">Set-AzApiManagement</span></span>

## <span data-ttu-id="e23e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e23e9-102">SYNOPSIS</span></span>
<span data-ttu-id="e23e9-103">Azure Api Management szolgáltatás frissítése</span><span class="sxs-lookup"><span data-stu-id="e23e9-103">Updates an Azure Api Management service</span></span>

## <span data-ttu-id="e23e9-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e23e9-104">SYNTAX</span></span>

```
Set-AzApiManagement -InputObject <PsApiManagement> [-SystemAssignedIdentity] [-UserAssignedIdentity <String[]>]
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e23e9-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e23e9-105">DESCRIPTION</span></span>

<span data-ttu-id="e23e9-106">A **Set-AzApiManagement** parancsmag frissíti az Azure API Management szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="e23e9-106">The **Set-AzApiManagement** cmdlet updates an Azure API Management service.</span></span>

## <span data-ttu-id="e23e9-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e23e9-107">EXAMPLES</span></span>

### <span data-ttu-id="e23e9-108">1. példa: API-kezelési szolgáltatás lekérte és prémium verzióra való méretezése és régió hozzáadása</span><span class="sxs-lookup"><span data-stu-id="e23e9-108">Example 1: Get an API Management service and scale it to Premium and Add a region</span></span>
```powershell
PS C:\> $apim = Get-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
PS C:\> $apim.Sku = "Premium"
PS C:\> $apim.Capacity = 5
PS C:\> $apim.AddRegion("Central US", "Premium", 3)
PS C:\>Set-AzApiManagement -InputObject $apim
```

<span data-ttu-id="e23e9-109">Ez a példa egy Api Management-példányt kap, azt öt prémium egységre méretezve, majd további három egységet ad hozzá a prémium régióhoz.</span><span class="sxs-lookup"><span data-stu-id="e23e9-109">This example gets an Api Management instance, scales it to five premium units and then adds an additional three units to the premium region.</span></span>

### <span data-ttu-id="e23e9-110">2. példa: Telepítés frissítése (külső VNET)</span><span class="sxs-lookup"><span data-stu-id="e23e9-110">Example 2: Update deployment (external VNET)</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzApiManagementVirtualNetwork -Location "East US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/Api-Default-WestUS/providers/Microsoft.Network/virtualNetworks/dfVirtualNetwork/subnets/backendSubnet"
PS C:\> $apim = Get-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
PS C:\> $apim.VpnType = "External"
PS C:\> $apim.VirtualNetwork = $virtualNetwork
PS C:\> Set-AzApiManagement -InputObject $apim
```

<span data-ttu-id="e23e9-111">Ez a parancs frissíti a meglévő API Management-telepítést, és egy külső *VpnType-hoz csatlakozik.*</span><span class="sxs-lookup"><span data-stu-id="e23e9-111">This command updates an existing API Management deployment and joins to an external *VpnType*.</span></span>

### <span data-ttu-id="e23e9-112">3. példa: A PsApiManagementCustomHostNameConfiguration példány létrehozása és inicializálása KeyVault-erőforrásból származó titkos mező használatával</span><span class="sxs-lookup"><span data-stu-id="e23e9-112">Example 3: Create and initialize an instance of PsApiManagementCustomHostNameConfiguration using an Secret from KeyVault Resource</span></span>
```powershell
PS C:\>$portal = New-AzApiManagementCustomHostnameConfiguration -Hostname "portal.contoso.com" -HostnameType Portal -KeyVaultId "https://apim-test-keyvault.vault.azure.net/secrets/api-portal-custom-ssl.pfx"
PS C:\>$proxy1 = New-AzApiManagementCustomHostnameConfiguration -Hostname "gatewayl.contoso.com" -HostnameType Proxy -KeyVaultId "https://apim-test-keyvault.vault.azure.net/secrets/contoso-proxy-custom-ssl.pfx"
PS C:\>$proxy2 = New-AzApiManagementCustomHostnameConfiguration -Hostname "gatewayl.foobar.com" -HostnameType Proxy -KeyVaultId "https://apim-test-keyvault.vault.azure.net/secrets/foobar-proxy-custom-ssl.pfx"
PS C:\>$proxyCustomConfig = @($proxy1,$proxy2)
PS C:\>$apim = Get-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
PS C:\>$apim.PortalCustomHostnameConfiguration = $portal
PS C:\>$apim.ProxyCustomHostnameConfiguration = $proxyCustomConfig 
PS C:\>Set-AzApiManagement -InputObject $apim -SystemAssignedIdentity
```

### <span data-ttu-id="e23e9-113">4. példa: A Publisher e-mail-címének, az NotificationSender e-mail-címének és a szervezet nevének frissítése</span><span class="sxs-lookup"><span data-stu-id="e23e9-113">Example 4: Update Publisher Email, NotificationSender Email and Organization Name</span></span>
```powershell
PS C:\> $apim = Get-AzApiManagement -ResourceGroupName "api-Default-West-US" -Name "Contoso"
PS C:\> $apim.PublisherEmail = "foobar@contoso.com"
PS C:\> $apim.NotificationSenderEmail = "notification@contoso.com"
PS C:\> $apim.OrganizationName = "Contoso"
PS C:\> Set-AzApiManagement -InputObject $apim -PassThru
```

## <span data-ttu-id="e23e9-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e23e9-114">PARAMETERS</span></span>

### <span data-ttu-id="e23e9-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e23e9-115">-AsJob</span></span>
<span data-ttu-id="e23e9-116">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="e23e9-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e23e9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e23e9-117">-DefaultProfile</span></span>
<span data-ttu-id="e23e9-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e23e9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e23e9-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e23e9-119">-InputObject</span></span>
<span data-ttu-id="e23e9-120">Az ApiManagement-példány.</span><span class="sxs-lookup"><span data-stu-id="e23e9-120">The ApiManagement instance.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e23e9-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e23e9-121">-PassThru</span></span>
<span data-ttu-id="e23e9-122">Frissített PsApiManagement-adatokat küld a folyamatnak, ha a művelet sikeres.</span><span class="sxs-lookup"><span data-stu-id="e23e9-122">Sends updated PsApiManagement to pipeline if operation succeeds.</span></span>

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

### <span data-ttu-id="e23e9-123">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="e23e9-123">-SystemAssignedIdentity</span></span>
<span data-ttu-id="e23e9-124">Azure Active Directory-identitás létrehozása és hozzárendelése ehhez a kiszolgálóhoz olyan kulcskezelő szolgáltatásokhoz, mint az Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="e23e9-124">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="e23e9-125">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="e23e9-125">-UserAssignedIdentity</span></span>
<span data-ttu-id="e23e9-126">Felhasználói identitásokat rendelhet ehhez a kiszolgálóhoz, hogy olyan kulcskezelő szolgáltatásokkal használja őket, mint az Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="e23e9-126">Assign User Identities to this server for use with key management services like Azure KeyVault.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e23e9-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e23e9-127">-Confirm</span></span>
<span data-ttu-id="e23e9-128">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="e23e9-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e23e9-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e23e9-129">-WhatIf</span></span>
<span data-ttu-id="e23e9-130">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="e23e9-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e23e9-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e23e9-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e23e9-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e23e9-132">CommonParameters</span></span>
<span data-ttu-id="e23e9-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e23e9-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e23e9-134">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e23e9-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e23e9-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e23e9-135">INPUTS</span></span>

### <span data-ttu-id="e23e9-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="e23e9-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="e23e9-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e23e9-137">OUTPUTS</span></span>

### <span data-ttu-id="e23e9-138">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="e23e9-138">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="e23e9-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e23e9-139">NOTES</span></span>

## <span data-ttu-id="e23e9-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e23e9-140">RELATED LINKS</span></span>

[<span data-ttu-id="e23e9-141">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="e23e9-141">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)

[<span data-ttu-id="e23e9-142">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="e23e9-142">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="e23e9-143">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="e23e9-143">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)
