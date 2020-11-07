---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagement.md
ms.openlocfilehash: 3831be3072f6922ad986cbde5a0a800764d1656a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679209"
---
# <span data-ttu-id="e83eb-101">Set-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="e83eb-101">Set-AzureRmApiManagement</span></span>

## <span data-ttu-id="e83eb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e83eb-102">SYNOPSIS</span></span>
<span data-ttu-id="e83eb-103">Azure API-kezelési szolgáltatás frissítése</span><span class="sxs-lookup"><span data-stu-id="e83eb-103">Updates an Azure Api Management service</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e83eb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e83eb-104">SYNTAX</span></span>

```
Set-AzureRmApiManagement -InputObject <PsApiManagement> [-AssignIdentity] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e83eb-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e83eb-105">DESCRIPTION</span></span>

<span data-ttu-id="e83eb-106">A **set-AzureRmApiManagement** parancsmag egy Azure API-kezelési szolgáltatást frissít.</span><span class="sxs-lookup"><span data-stu-id="e83eb-106">The **Set-AzureRmApiManagement** cmdlet updates an Azure API Management service.</span></span>

## <span data-ttu-id="e83eb-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e83eb-107">EXAMPLES</span></span>

### <span data-ttu-id="e83eb-108">Példa 1 API-kezelési szolgáltatás beszerzése és átméretezése a prémium verzióhoz és a régió hozzáadásához</span><span class="sxs-lookup"><span data-stu-id="e83eb-108">Example 1 Get an API Management service and scale it to Premium and Add a region</span></span>
```powershell
PS C:\> $apim = Get-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
PS C:\> $apim.Sku = "Premium"
PS C:\> $apim.Capacity = 5
PS C:\> $apim.AddRegion("Central US", "Premium", 3)
PS C:\>Set-AzureRmApiManagement -ApiManagement $apim
```

<span data-ttu-id="e83eb-109">Ebben a példában egy API-kezelési példány válik, és öt prémium egységre méretezi, majd egy további három egységet ad hozzá a prémium régióhoz.</span><span class="sxs-lookup"><span data-stu-id="e83eb-109">This example gets an Api Management instance, scales it to five premium units and then adds an additional three units to the premium region.</span></span>

### <span data-ttu-id="e83eb-110">2. példa: a frissítés telepítése (külső VNET)</span><span class="sxs-lookup"><span data-stu-id="e83eb-110">Example 2: Update deployment (external VNET)</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "East US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/Api-Default-WestUS/providers/Microsoft.Network/virtualNetworks/dfVirtualNetwork/subnets/backendSubnet"
PS C:\> $apim = Get-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
PS C:\> $apim.VpnType = "External"
PS C:\> $apim.VirtualNetwork = $virtualNetwork
PS C:\> Set-AzureRmApiManagement -ApiManagement $apim
```

<span data-ttu-id="e83eb-111">Ez a parancs frissíti egy meglévő API-kezelési telepítőt, és csatlakozik egy külső *VpnType*.</span><span class="sxs-lookup"><span data-stu-id="e83eb-111">This command updates an existing API Management deployment and joins to an external *VpnType*.</span></span>

### <span data-ttu-id="e83eb-112">3. példa: a PsApiManagementCustomHostNameConfiguration-példányok létrehozása és inicializálása titkos kulccsal</span><span class="sxs-lookup"><span data-stu-id="e83eb-112">Example 3: Create and initialize an instance of PsApiManagementCustomHostNameConfiguration using an Secret from KeyVault Resource</span></span>
```powershell
PS C:\>$portal = New-AzureRmApiManagementCustomHostnameConfiguration -Hostname "portal.contoso.com" -HostnameType Portal -KeyVaultId "https://apim-test-keyvault.vault.azure.net/secrets/api-portal-custom-ssl.pfx"
PS C:\>$proxy1 = New-AzureRmApiManagementCustomHostnameConfiguration -Hostname "gatewayl.contoso.com" -HostnameType Proxy -KeyVaultId "https://apim-test-keyvault.vault.azure.net/secrets/contoso-proxy-custom-ssl.pfx"
PS C:\>$proxy2 = New-AzureRmApiManagementCustomHostnameConfiguration -Hostname "gatewayl.foobar.com" -HostnameType Proxy -KeyVaultId "https://apim-test-keyvault.vault.azure.net/secrets/foobar-proxy-custom-ssl.pfx"
PS C:\>$proxyCustomConfig = @($proxy1,$proxy2)
PS C:\>$apim = Get-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
PS C:\>$apim.PortalCustomHostnameConfiguration = $portal
PS C:\>$apim.ProxyCustomHostnameConfiguration = $proxyCustomConfig 
PS C:\>Set-AzureRmApiManagement -InputObject $apim -AssignIdentity
```

## <span data-ttu-id="e83eb-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e83eb-113">PARAMETERS</span></span>

### <span data-ttu-id="e83eb-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e83eb-114">-AsJob</span></span>
<span data-ttu-id="e83eb-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="e83eb-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e83eb-116">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="e83eb-116">-AssignIdentity</span></span>
<span data-ttu-id="e83eb-117">Hozzon létre és rendeljen hozzá egy Azure Active Directory-identitást a kiszolgálóhoz a kulcskezelő szolgáltatásokhoz (például Azure kulcskezelő) való használatra.</span><span class="sxs-lookup"><span data-stu-id="e83eb-117">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="e83eb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e83eb-118">-DefaultProfile</span></span>
<span data-ttu-id="e83eb-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e83eb-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e83eb-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e83eb-120">-InputObject</span></span>
<span data-ttu-id="e83eb-121">A ApiManagement példány.</span><span class="sxs-lookup"><span data-stu-id="e83eb-121">The ApiManagement instance.</span></span>

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

### <span data-ttu-id="e83eb-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e83eb-122">-PassThru</span></span>
<span data-ttu-id="e83eb-123">Frissített PsApiManagement küld a csővezetéknek, ha a művelet sikeres.</span><span class="sxs-lookup"><span data-stu-id="e83eb-123">Sends updated PsApiManagement to pipeline if operation succeeds.</span></span>

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

### <span data-ttu-id="e83eb-124">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e83eb-124">-Confirm</span></span>
<span data-ttu-id="e83eb-125">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e83eb-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e83eb-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e83eb-126">-WhatIf</span></span>
<span data-ttu-id="e83eb-127">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e83eb-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e83eb-128">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e83eb-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e83eb-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e83eb-129">CommonParameters</span></span>
<span data-ttu-id="e83eb-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e83eb-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e83eb-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e83eb-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e83eb-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e83eb-132">INPUTS</span></span>

### <span data-ttu-id="e83eb-133">Microsoft. Azure. Command. ApiManagement. models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="e83eb-133">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>
<span data-ttu-id="e83eb-134">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e83eb-134">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="e83eb-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e83eb-135">OUTPUTS</span></span>

### <span data-ttu-id="e83eb-136">Microsoft. Azure. Command. ApiManagement. models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="e83eb-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="e83eb-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e83eb-137">NOTES</span></span>

## <span data-ttu-id="e83eb-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e83eb-138">RELATED LINKS</span></span>

[<span data-ttu-id="e83eb-139">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="e83eb-139">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)

[<span data-ttu-id="e83eb-140">Új – AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="e83eb-140">New-AzureRmApiManagement</span></span>](./New-AzureRmApiManagement.md)

[<span data-ttu-id="e83eb-141">Remove-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="e83eb-141">Remove-AzureRmApiManagement</span></span>](./Remove-AzureRmApiManagement.md)
