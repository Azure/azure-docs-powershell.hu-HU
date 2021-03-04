---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D341
online version: https://docs.microsoft.com/powershell/module/az.trafficmanager/add-aztrafficmanagerIpAddressRange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerIpAddressRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerIpAddressRange.md
ms.openlocfilehash: 84d994366c81b7adfc5fa0f7fdb34267ae8b6370
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918034"
---
# <span data-ttu-id="8f5a9-101">Add-AzTrafficManagerIpAddressRange</span><span class="sxs-lookup"><span data-stu-id="8f5a9-101">Add-AzTrafficManagerIpAddressRange</span></span>

## <span data-ttu-id="8f5a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f5a9-102">SYNOPSIS</span></span>
<span data-ttu-id="8f5a9-103">Címtartományt vagy alhálózatot ad hozzá egy helyi Traffic Manager-végpontobjektumhoz.</span><span class="sxs-lookup"><span data-stu-id="8f5a9-103">Adds an address range or subnet to a local Traffic Manager endpoint object.</span></span>

## <span data-ttu-id="8f5a9-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8f5a9-104">SYNTAX</span></span>

```
Add-AzTrafficManagerIpAddressRange -First <String> [-Last <String>] [-Scope <Int32>]
 -TrafficManagerEndpoint <TrafficManagerEndpoint> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f5a9-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8f5a9-105">DESCRIPTION</span></span>
<span data-ttu-id="8f5a9-106">Az **Add-AzTrafficManagerIpAddressRange** parancsmag hozzáad egy IP-címtartományt egy helyi Azure Traffic Manager-végpontobjektumhoz.</span><span class="sxs-lookup"><span data-stu-id="8f5a9-106">The **Add-AzTrafficManagerIpAddressRange** cmdlet adds an IP address range to a local Azure Traffic Manager endpoint object.</span></span>
<span data-ttu-id="8f5a9-107">Végpontot a New-AzTrafficManagerEndpoint parancsmagok Get-AzTrafficManagerEndpoint le.</span><span class="sxs-lookup"><span data-stu-id="8f5a9-107">You can get an endpoint by using the New-AzTrafficManagerEndpoint or Get-AzTrafficManagerEndpoint cmdlets.</span></span>

<span data-ttu-id="8f5a9-108">Ez a parancsmag a helyi végpontobjektumon működik.</span><span class="sxs-lookup"><span data-stu-id="8f5a9-108">This cmdlet operates on the local endpoint object.</span></span>
<span data-ttu-id="8f5a9-109">A Módosítások véglegesítése a Forgalomkezelő végpontjára a Set-AzTrafficManagerEndpoint parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="8f5a9-109">Commit your changes to the endpoint for Traffic Manager by using the Set-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="8f5a9-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8f5a9-110">EXAMPLES</span></span>

### <span data-ttu-id="8f5a9-111">1. példa: IP-címtartományok hozzáadása végponthoz</span><span class="sxs-lookup"><span data-stu-id="8f5a9-111">Example 1: Add IP address ranges to an endpoint</span></span>
```
PS C:\> $TrafficManagerEndpoint = New-AzTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints -Priority 1 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-CentralUS/providers/Microsoft.Web/sites/contoso-web-app" -Weight 10
PS C:\> Add-AzTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "1.2.3.4" -Last "5.6.7.8"
PS C:\> Add-AzTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "9.10.11.0" -Scope 24
PS C:\> Add-AzTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "12.13.14.0" -Last "12.13.14.31" -Scope 27
PS C:\> Add-AzTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "15.16.17.18"
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="8f5a9-112">Az első parancs egy Azure Traffic Manager-végpontot hoz létre a **New-AzTrafficManagerEndpoint** parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="8f5a9-112">The first command creates an Azure Traffic Manager endpoint by using the **New-AzTrafficManagerEndpoint** cmdlet.</span></span>
<span data-ttu-id="8f5a9-113">A parancs a helyi végpontot a $TrafficManagerEndpoint tárolja.</span><span class="sxs-lookup"><span data-stu-id="8f5a9-113">The command stores the local endpoint in the $TrafficManagerEndpoint variable.</span></span>
<span data-ttu-id="8f5a9-114">A második parancs hozzáadja az 1.2.3.4-es IP-címtartományt az 5.6.7.8 tartományhoz a $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="8f5a9-114">The second command adds the IP address range 1.2.3.4 to 5.6.7.8 to the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="8f5a9-115">A harmadik parancs hozzáadja a 9.10.11.0 IP-címtartományt a 9.10.11.255 tartományhoz a $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="8f5a9-115">The third command adds the IP address range 9.10.11.0 to 9.10.11.255 to the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="8f5a9-116">A negyedik parancs ellenőrzi, hogy a tartomány mérete megegyezik-e a tartomány méretével, majd hozzáadja a 12.13.14.0 ip-címtartományt a 12.13.14.31 tartományhoz a $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="8f5a9-116">The fourth command verifies that the scope matches the size of the range, then adds the IP address range 12.13.14.0 to 12.13.14.31 to the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="8f5a9-117">Az ötödik parancs hozzáadja a 15.16.17.18 és a 15.16.17.18 IP-címtartományt a $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="8f5a9-117">The fifth command adds the IP address range 15.16.17.18 to 15.16.17.18 to the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="8f5a9-118">Az utolsó parancs frissíti a Traffic Managerben a végpontot úgy, hogy megfeleljen a helyi $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="8f5a9-118">The final command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="8f5a9-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8f5a9-119">PARAMETERS</span></span>

### <span data-ttu-id="8f5a9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f5a9-120">-DefaultProfile</span></span>
<span data-ttu-id="8f5a9-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8f5a9-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8f5a9-122">-Last</span><span class="sxs-lookup"><span data-stu-id="8f5a9-122">-Last</span></span>
<span data-ttu-id="8f5a9-123">A hozzáadható tartomány utolsó IP-címe.</span><span class="sxs-lookup"><span data-stu-id="8f5a9-123">Specifies the last IP address in the range to be added.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f5a9-124">-Scope</span><span class="sxs-lookup"><span data-stu-id="8f5a9-124">-Scope</span></span>
<span data-ttu-id="8f5a9-125">A hozzáadható IP-címtartomány hatókörét határozza meg.</span><span class="sxs-lookup"><span data-stu-id="8f5a9-125">Specifies the scope of the IP address range to be added.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f5a9-126">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="8f5a9-126">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="8f5a9-127">Helyi **TrafficManagerEndpoint-objektumot ad** meg.</span><span class="sxs-lookup"><span data-stu-id="8f5a9-127">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="8f5a9-128">Ez a parancsmag módosítja ezt a helyi objektumot.</span><span class="sxs-lookup"><span data-stu-id="8f5a9-128">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="8f5a9-129">A **TrafficManagerEndpoint** objektum beszerzéséhez használja a Get-AzTrafficManagerEndpoint vagy New-AzTrafficManagerEndpoint parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="8f5a9-129">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint or New-AzTrafficManagerEndpoint cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8f5a9-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8f5a9-130">-Confirm</span></span>
<span data-ttu-id="8f5a9-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="8f5a9-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f5a9-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f5a9-132">-WhatIf</span></span>
<span data-ttu-id="8f5a9-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="8f5a9-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8f5a9-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8f5a9-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f5a9-135">-First</span><span class="sxs-lookup"><span data-stu-id="8f5a9-135">-First</span></span>
<span data-ttu-id="8f5a9-136">A hozzáadható tartomány első IP-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8f5a9-136">Specifies the first IP address in the range to be added.</span></span>

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

### <span data-ttu-id="8f5a9-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f5a9-137">CommonParameters</span></span>
<span data-ttu-id="8f5a9-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f5a9-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f5a9-139">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f5a9-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f5a9-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8f5a9-140">INPUTS</span></span>

### <span data-ttu-id="8f5a9-141">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="8f5a9-141">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="8f5a9-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8f5a9-142">OUTPUTS</span></span>

### <span data-ttu-id="8f5a9-143">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="8f5a9-143">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="8f5a9-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8f5a9-144">NOTES</span></span>

## <span data-ttu-id="8f5a9-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8f5a9-145">RELATED LINKS</span></span>

[<span data-ttu-id="8f5a9-146">Remove-AzTrafficManagerIpAddressRange</span><span class="sxs-lookup"><span data-stu-id="8f5a9-146">Remove-AzTrafficManagerIpAddressRange</span></span>](./Remove-AzTrafficManagerIpAddressRange.md)

[<span data-ttu-id="8f5a9-147">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="8f5a9-147">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="8f5a9-148">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="8f5a9-148">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="8f5a9-149">Set-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="8f5a9-149">Set-AzTrafficManagerEndpoint</span></span>](./Set-AzTrafficManagerEndpoint.md)
