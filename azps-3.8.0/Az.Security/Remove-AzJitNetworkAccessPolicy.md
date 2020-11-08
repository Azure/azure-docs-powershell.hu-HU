---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzJitNetworkAccessPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzJitNetworkAccessPolicy.md
ms.openlocfilehash: 21a31d2d4e094e986ad862bfe69baef98148e5f0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011587"
---
# <span data-ttu-id="572e2-101">Remove-AzJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="572e2-101">Remove-AzJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="572e2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="572e2-102">SYNOPSIS</span></span>
<span data-ttu-id="572e2-103">A JIT-hálózat hozzáférési házirendjének törlése</span><span class="sxs-lookup"><span data-stu-id="572e2-103">Deletes a JIT network access policy.</span></span>

## <span data-ttu-id="572e2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="572e2-104">SYNTAX</span></span>

### <span data-ttu-id="572e2-105">ResourceGroupLevelResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="572e2-105">ResourceGroupLevelResource (Default)</span></span>
```
Remove-AzJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="572e2-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="572e2-106">ResourceId</span></span>
```
Remove-AzJitNetworkAccessPolicy -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="572e2-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="572e2-107">InputObject</span></span>
```
Remove-AzJitNetworkAccessPolicy -InputObject <PSSecurityJitNetworkAccessPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="572e2-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="572e2-108">DESCRIPTION</span></span>
<span data-ttu-id="572e2-109">Csak az időpontos hálózati hozzáférés házirendjének törlése</span><span class="sxs-lookup"><span data-stu-id="572e2-109">Deletes a Just In Time network access policy.</span></span>
<span data-ttu-id="572e2-110">Ezt követően a felhasználó nem tud ideiglenes hálózati kapcsolatot kérni a törölt házirenden belül konfigurált VMs-kapcsolaton.</span><span class="sxs-lookup"><span data-stu-id="572e2-110">After this action a user will not be able to request temporary network connection on the VMs that were configured inside the deleted policy.</span></span>

## <span data-ttu-id="572e2-111">Példák</span><span class="sxs-lookup"><span data-stu-id="572e2-111">EXAMPLES</span></span>

### <span data-ttu-id="572e2-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="572e2-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default"
```

<span data-ttu-id="572e2-113">Csak az időpontos hálózati hozzáférés házirendjének törlése</span><span class="sxs-lookup"><span data-stu-id="572e2-113">Deletes a Just In Time network access policy.</span></span>

## <span data-ttu-id="572e2-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="572e2-114">PARAMETERS</span></span>

### <span data-ttu-id="572e2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="572e2-115">-DefaultProfile</span></span>
<span data-ttu-id="572e2-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="572e2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="572e2-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="572e2-117">-InputObject</span></span>
<span data-ttu-id="572e2-118">Beviteli objektum</span><span class="sxs-lookup"><span data-stu-id="572e2-118">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="572e2-119">-Hely</span><span class="sxs-lookup"><span data-stu-id="572e2-119">-Location</span></span>
<span data-ttu-id="572e2-120">Helyre.</span><span class="sxs-lookup"><span data-stu-id="572e2-120">Location.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="572e2-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="572e2-121">-Name</span></span>
<span data-ttu-id="572e2-122">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="572e2-122">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="572e2-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="572e2-123">-PassThru</span></span>
<span data-ttu-id="572e2-124">Adja meg, hogy a művelet sikeres volt-e.</span><span class="sxs-lookup"><span data-stu-id="572e2-124">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="572e2-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="572e2-125">-ResourceGroupName</span></span>
<span data-ttu-id="572e2-126">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="572e2-126">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="572e2-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="572e2-127">-ResourceId</span></span>
<span data-ttu-id="572e2-128">Erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="572e2-128">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="572e2-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="572e2-129">-Confirm</span></span>
<span data-ttu-id="572e2-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="572e2-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="572e2-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="572e2-131">-WhatIf</span></span>
<span data-ttu-id="572e2-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="572e2-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="572e2-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="572e2-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="572e2-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="572e2-134">CommonParameters</span></span>
<span data-ttu-id="572e2-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="572e2-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="572e2-136">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="572e2-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="572e2-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="572e2-137">INPUTS</span></span>

### <span data-ttu-id="572e2-138">System. String</span><span class="sxs-lookup"><span data-stu-id="572e2-138">System.String</span></span>

### <span data-ttu-id="572e2-139">Microsoft. Azure. commands. Security. models. JitNetworkAccessPolicies. PSSecurityJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="572e2-139">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="572e2-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="572e2-140">OUTPUTS</span></span>

### <span data-ttu-id="572e2-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="572e2-141">System.Boolean</span></span>

## <span data-ttu-id="572e2-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="572e2-142">NOTES</span></span>

## <span data-ttu-id="572e2-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="572e2-143">RELATED LINKS</span></span>
