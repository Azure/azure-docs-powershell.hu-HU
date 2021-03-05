---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/powershell/module/az.websites/new-azappserviceenvironmentinboundservices
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzAppServiceEnvironmentInboundServices.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzAppServiceEnvironmentInboundServices.md
ms.openlocfilehash: 68b2957e959365187ad82980bd2be2f055632a57
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002117"
---
# <span data-ttu-id="83629-101">New-AzAppServiceEnvironmentInboundServices</span><span class="sxs-lookup"><span data-stu-id="83629-101">New-AzAppServiceEnvironmentInboundServices</span></span>

## <span data-ttu-id="83629-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="83629-102">SYNOPSIS</span></span>
<span data-ttu-id="83629-103">Bejövő szolgáltatásokat hoz létre az app szolgáltatási környezetéhez.</span><span class="sxs-lookup"><span data-stu-id="83629-103">Creates inbound services for App Service Environment.</span></span> <span data-ttu-id="83629-104">Az ASEv2 ILB esetén ez létrehoz egy Azure Private DNS-zónát, és a belső IP-címnek megfelelő rekordokat hoz létre.</span><span class="sxs-lookup"><span data-stu-id="83629-104">For ASEv2 ILB, this will create an Azure Private DNS Zone and records to map to the internal IP.</span></span> <span data-ttu-id="83629-105">Az ASEv3 esetén továbbá gondoskodni fog arról, hogy az alhálózat letiltotta a hálózati házirendet, és létrehozzon egy privát végpontot.</span><span class="sxs-lookup"><span data-stu-id="83629-105">For ASEv3 it will in addition ensure subnet has Network Policy disabled and will create a private endpoint.</span></span>

## <span data-ttu-id="83629-106">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="83629-106">SYNTAX</span></span>

### <span data-ttu-id="83629-107">SubnetNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="83629-107">SubnetNameParameterSet</span></span>
```
New-AzAppServiceEnvironmentInboundServices [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkName <String> -SubnetName <String> [-SkipDns] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83629-108">SubnetIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="83629-108">SubnetIdParameterSet</span></span>
```
New-AzAppServiceEnvironmentInboundServices [-ResourceGroupName] <String> [-Name] <String> -SubnetId <String>
 [-SkipDns] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="83629-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="83629-109">DESCRIPTION</span></span>
<span data-ttu-id="83629-110">A **New-AzAppServiceEnvironmentInboundServices** parancsmag bejövő szolgáltatásokat hoz létre az appszolgáltatási környezethez.</span><span class="sxs-lookup"><span data-stu-id="83629-110">The **New-AzAppServiceEnvironmentInboundServices** cmdlet create inbound services for an App Service Environment.</span></span>

## <span data-ttu-id="83629-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="83629-111">EXAMPLES</span></span>

### <span data-ttu-id="83629-112">1. példa: Privát DNS-zóna és rekordok létrehozása az ASEv2 szolgáltatáshoz</span><span class="sxs-lookup"><span data-stu-id="83629-112">Example 1: Create Private DNS Zone and records for ASEv2</span></span>
```powershell
PS C:\> New-AzAppServiceEnvironmentInboundServices -ResourceGroupName AseResourceGroup -Name AseV2Name
-VirtualNetworkName MyVirtualNetwork -SubnetName InboundSubnet
```

<span data-ttu-id="83629-113">Create Private DNS Zone and records for ASEv2</span><span class="sxs-lookup"><span data-stu-id="83629-113">Create Private DNS Zone and records for ASEv2</span></span>

### <span data-ttu-id="83629-114">2. példa: Privát végpont, privát DNS-zóna és ASEv3-rekordok létrehozása</span><span class="sxs-lookup"><span data-stu-id="83629-114">Example 2: Create private endpoint, Private DNS Zone and records for ASEv3</span></span>
```powershell
PS C:\> New-AzAppServiceEnvironmentInboundServices -ResourceGroupName AseResourceGroup -Name AseV2Name
-VirtualNetworkName MyVirtualNetwork -SubnetName InboundSubnet
```

<span data-ttu-id="83629-115">Create private endpoint, Private DNS Zone and records for ASEv3</span><span class="sxs-lookup"><span data-stu-id="83629-115">Create private endpoint, Private DNS Zone and records for ASEv3</span></span>

### <span data-ttu-id="83629-116">3. példa: Privát végpont létrehozása az ASEv3-hoz</span><span class="sxs-lookup"><span data-stu-id="83629-116">Example 3: Create private endpoint for ASEv3</span></span>
```powershell
PS C:\> New-AzAppServiceEnvironmentInboundServices -ResourceGroupName AseResourceGroup -Name AseV2Name
-VirtualNetworkName MyVirtualNetwork -SubnetName InboundSubnet -SkipDns
```

<span data-ttu-id="83629-117">Privát végpont létrehozása AZ ASEv3-hoz</span><span class="sxs-lookup"><span data-stu-id="83629-117">Create private endpoint for ASEv3</span></span>

## <span data-ttu-id="83629-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="83629-118">PARAMETERS</span></span>

### <span data-ttu-id="83629-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83629-119">-DefaultProfile</span></span>
<span data-ttu-id="83629-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="83629-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="83629-121">-Name</span><span class="sxs-lookup"><span data-stu-id="83629-121">-Name</span></span>
<span data-ttu-id="83629-122">Az app szolgáltatási környezetének neve.</span><span class="sxs-lookup"><span data-stu-id="83629-122">The name of the app service environment.</span></span>

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

### <span data-ttu-id="83629-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="83629-123">-PassThru</span></span>
<span data-ttu-id="83629-124">Visszaküldés állapota.</span><span class="sxs-lookup"><span data-stu-id="83629-124">Return status.</span></span>

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

### <span data-ttu-id="83629-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83629-125">-ResourceGroupName</span></span>
<span data-ttu-id="83629-126">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="83629-126">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83629-127">-SkipDns</span><span class="sxs-lookup"><span data-stu-id="83629-127">-SkipDns</span></span>
<span data-ttu-id="83629-128">Ne hozzon létre Azure Private DNS Zone-t és -rekordokat.</span><span class="sxs-lookup"><span data-stu-id="83629-128">Do not create Azure Private DNS Zone and records.</span></span>

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

### <span data-ttu-id="83629-129">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="83629-129">-SubnetId</span></span>
<span data-ttu-id="83629-130">Az alhálózat azonosítója.</span><span class="sxs-lookup"><span data-stu-id="83629-130">The subnet id.</span></span>

```yaml
Type: System.String
Parameter Sets: SubnetIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83629-131">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="83629-131">-SubnetName</span></span>
<span data-ttu-id="83629-132">Az alhálózat neve.</span><span class="sxs-lookup"><span data-stu-id="83629-132">The subnet name.</span></span> <span data-ttu-id="83629-133">A -VirtualNetworkName névvel együtt használható, és az ASE-val azonos erőforráscsoportban kell lennie.</span><span class="sxs-lookup"><span data-stu-id="83629-133">Used in combination with -VirtualNetworkName and must be in same resource group as ASE.</span></span> <span data-ttu-id="83629-134">Ha nem, használja az -SubnetId</span><span class="sxs-lookup"><span data-stu-id="83629-134">If not, use -SubnetId</span></span>

```yaml
Type: System.String
Parameter Sets: SubnetNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83629-135">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="83629-135">-VirtualNetworkName</span></span>
<span data-ttu-id="83629-136">A vNet neve.</span><span class="sxs-lookup"><span data-stu-id="83629-136">The vNet name.</span></span> <span data-ttu-id="83629-137">-Alhálózatnévvel együtt használható, és az ASE-val azonos erőforráscsoportban kell lennie.</span><span class="sxs-lookup"><span data-stu-id="83629-137">Used in combination with -SubnetName and must be in same resource group as ASE.</span></span> <span data-ttu-id="83629-138">Ha nem, használja az -SubnetId</span><span class="sxs-lookup"><span data-stu-id="83629-138">If not, use -SubnetId</span></span>

```yaml
Type: System.String
Parameter Sets: SubnetNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83629-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="83629-139">-Confirm</span></span>
<span data-ttu-id="83629-140">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="83629-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83629-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83629-141">-WhatIf</span></span>
<span data-ttu-id="83629-142">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="83629-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83629-143">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="83629-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83629-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83629-144">CommonParameters</span></span>
<span data-ttu-id="83629-145">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83629-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83629-146">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="83629-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83629-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="83629-147">INPUTS</span></span>

### <span data-ttu-id="83629-148">Nincs</span><span class="sxs-lookup"><span data-stu-id="83629-148">None</span></span>

## <span data-ttu-id="83629-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="83629-149">OUTPUTS</span></span>

### <span data-ttu-id="83629-150">System.Object</span><span class="sxs-lookup"><span data-stu-id="83629-150">System.Object</span></span>
## <span data-ttu-id="83629-151">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="83629-151">NOTES</span></span>

## <span data-ttu-id="83629-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="83629-152">RELATED LINKS</span></span>

[<span data-ttu-id="83629-153">New-AzAppServiceEnvironment</span><span class="sxs-lookup"><span data-stu-id="83629-153">New-AzAppServiceEnvironment</span></span>](./New-AzAppServiceEnvironment.md)

[<span data-ttu-id="83629-154">Get-AzAppServiceEnvironment</span><span class="sxs-lookup"><span data-stu-id="83629-154">Get-AzAppServiceEnvironment</span></span>](./Get-AzAppServiceEnvironment.md)

[<span data-ttu-id="83629-155">Remove-AzAppServiceEnvironment</span><span class="sxs-lookup"><span data-stu-id="83629-155">Remove-AzAppServiceEnvironment</span></span>](./Remove-AzAppServiceEnvironment.md)