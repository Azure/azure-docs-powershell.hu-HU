---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagement.md
ms.openlocfilehash: c00e8e8d33ef0f7b7b2591287e9bda9bc876e3c0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94300890"
---
# <span data-ttu-id="aba64-101">Set-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="aba64-101">Set-AzApiManagement</span></span>

## <span data-ttu-id="aba64-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="aba64-102">SYNOPSIS</span></span>
<span data-ttu-id="aba64-103">Azure API-kezelési szolgáltatás frissítése</span><span class="sxs-lookup"><span data-stu-id="aba64-103">Updates an Azure Api Management service</span></span>

## <span data-ttu-id="aba64-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="aba64-104">SYNTAX</span></span>

```
Set-AzApiManagement -InputObject <PsApiManagement> [-SystemAssignedIdentity] [-UserAssignedIdentity <String[]>]
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aba64-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="aba64-105">DESCRIPTION</span></span>

<span data-ttu-id="aba64-106">A **set-AzApiManagement** parancsmag egy Azure API-kezelési szolgáltatást frissít.</span><span class="sxs-lookup"><span data-stu-id="aba64-106">The **Set-AzApiManagement** cmdlet updates an Azure API Management service.</span></span>

## <span data-ttu-id="aba64-107">Példák</span><span class="sxs-lookup"><span data-stu-id="aba64-107">EXAMPLES</span></span>

### <span data-ttu-id="aba64-108">Példa 1: API-kezelési szolgáltatás beszerzése és átméretezése a prémium verzióhoz és a régió hozzáadásához</span><span class="sxs-lookup"><span data-stu-id="aba64-108">Example 1: Get an API Management service and scale it to Premium and Add a region</span></span>
```powershell
PS C:\> $apim = Get-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
PS C:\> $apim.Sku = "Premium"
PS C:\> $apim.Capacity = 5
PS C:\> $apim.AddRegion("Central US", "Premium", 3)
PS C:\>Set-AzApiManagement -InputObject $apim
```

<span data-ttu-id="aba64-109">Ebben a példában egy API-kezelési példány válik, és öt prémium egységre méretezi, majd egy további három egységet ad hozzá a prémium régióhoz.</span><span class="sxs-lookup"><span data-stu-id="aba64-109">This example gets an Api Management instance, scales it to five premium units and then adds an additional three units to the premium region.</span></span>

### <span data-ttu-id="aba64-110">2. példa: a frissítés telepítése (külső VNET)</span><span class="sxs-lookup"><span data-stu-id="aba64-110">Example 2: Update deployment (external VNET)</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzApiManagementVirtualNetwork -Location "East US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/Api-Default-WestUS/providers/Microsoft.Network/virtualNetworks/dfVirtualNetwork/subnets/backendSubnet"
PS C:\> $apim = Get-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
PS C:\> $apim.VpnType = "External"
PS C:\> $apim.VirtualNetwork = $virtualNetwork
PS C:\> Set-AzApiManagement -InputObject $apim
```

<span data-ttu-id="aba64-111">Ez a parancs frissíti egy meglévő API-kezelési telepítőt, és csatlakozik egy külső *VpnType*.</span><span class="sxs-lookup"><span data-stu-id="aba64-111">This command updates an existing API Management deployment and joins to an external *VpnType*.</span></span>

### <span data-ttu-id="aba64-112">3. példa: a PsApiManagementCustomHostNameConfiguration-példányok létrehozása és inicializálása titkos kulccsal</span><span class="sxs-lookup"><span data-stu-id="aba64-112">Example 3: Create and initialize an instance of PsApiManagementCustomHostNameConfiguration using an Secret from KeyVault Resource</span></span>
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

### <span data-ttu-id="aba64-113">4. példa: a Publisher e-mail-címének frissítése, NotificationSender-és szervezeti név</span><span class="sxs-lookup"><span data-stu-id="aba64-113">Example 4: Update Publisher Email, NotificationSender Email and Organization Name</span></span>
```powershell
PS C:\> $apim = Get-AzApiManagement -ResourceGroupName "api-Default-West-US" -Name "Contoso"
PS C:\> $apim.PublisherEmail = "foobar@contoso.com"
PS C:\> $apim.NotificationSenderEmail = "notification@contoso.com"
PS C:\> $apim.OrganizationName = "Contoso"
PS C:\> Set-AzApiManagement -InputObject $apim -PassThru
```

## <span data-ttu-id="aba64-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="aba64-114">PARAMETERS</span></span>

### <span data-ttu-id="aba64-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="aba64-115">-AsJob</span></span>
<span data-ttu-id="aba64-116">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="aba64-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="aba64-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aba64-117">-DefaultProfile</span></span>
<span data-ttu-id="aba64-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="aba64-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aba64-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aba64-119">-InputObject</span></span>
<span data-ttu-id="aba64-120">A ApiManagement példány.</span><span class="sxs-lookup"><span data-stu-id="aba64-120">The ApiManagement instance.</span></span>

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

### <span data-ttu-id="aba64-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="aba64-121">-PassThru</span></span>
<span data-ttu-id="aba64-122">Frissített PsApiManagement küld a csővezetéknek, ha a művelet sikeres.</span><span class="sxs-lookup"><span data-stu-id="aba64-122">Sends updated PsApiManagement to pipeline if operation succeeds.</span></span>

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

### <span data-ttu-id="aba64-123">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="aba64-123">-SystemAssignedIdentity</span></span>
<span data-ttu-id="aba64-124">Hozzon létre és rendeljen hozzá egy Azure Active Directory-identitást a kiszolgálóhoz a kulcskezelő szolgáltatásokhoz (például Azure kulcskezelő) való használatra.</span><span class="sxs-lookup"><span data-stu-id="aba64-124">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="aba64-125">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="aba64-125">-UserAssignedIdentity</span></span>
<span data-ttu-id="aba64-126">Rendeljen hozzá felhasználói identitásokat a kiszolgálóhoz a kulcskezelő szolgáltatásokkal (például Azure kulcskezelő szolgáltatással) való használatra.</span><span class="sxs-lookup"><span data-stu-id="aba64-126">Assign User Identities to this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="aba64-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="aba64-127">-Confirm</span></span>
<span data-ttu-id="aba64-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="aba64-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aba64-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aba64-129">-WhatIf</span></span>
<span data-ttu-id="aba64-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="aba64-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="aba64-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="aba64-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aba64-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aba64-132">CommonParameters</span></span>
<span data-ttu-id="aba64-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="aba64-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aba64-134">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="aba64-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aba64-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="aba64-135">INPUTS</span></span>

### <span data-ttu-id="aba64-136">Microsoft. Azure. Command. ApiManagement. models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="aba64-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="aba64-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="aba64-137">OUTPUTS</span></span>

### <span data-ttu-id="aba64-138">Microsoft. Azure. Command. ApiManagement. models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="aba64-138">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="aba64-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="aba64-139">NOTES</span></span>

## <span data-ttu-id="aba64-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="aba64-140">RELATED LINKS</span></span>

[<span data-ttu-id="aba64-141">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="aba64-141">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)

[<span data-ttu-id="aba64-142">Új – AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="aba64-142">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="aba64-143">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="aba64-143">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)
