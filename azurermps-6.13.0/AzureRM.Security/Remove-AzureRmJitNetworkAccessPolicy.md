---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Remove-AzureRmJitNetworkAccessPolicy.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Remove-AzureRmJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Remove-AzureRmJitNetworkAccessPolicy.md
ms.openlocfilehash: 19de4ad776814efa55cdff19b2a77673d8581992
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494922"
---
# <span data-ttu-id="ea6f6-101">Remove-AzureRmJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ea6f6-101">Remove-AzureRmJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="ea6f6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ea6f6-102">SYNOPSIS</span></span>
<span data-ttu-id="ea6f6-103">A JIT-hálózat hozzáférési házirendjének törlése</span><span class="sxs-lookup"><span data-stu-id="ea6f6-103">Deletes a JIT network access policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ea6f6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ea6f6-104">SYNTAX</span></span>

### <span data-ttu-id="ea6f6-105">ResourceGroupLevelResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ea6f6-105">ResourceGroupLevelResource (Default)</span></span>
```
Remove-AzureRmJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea6f6-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="ea6f6-106">ResourceId</span></span>
```
Remove-AzureRmJitNetworkAccessPolicy -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea6f6-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="ea6f6-107">InputObject</span></span>
```
Remove-AzureRmJitNetworkAccessPolicy -InputObject <PSRemoveJitNetworkAccessPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea6f6-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="ea6f6-108">DESCRIPTION</span></span>
<span data-ttu-id="ea6f6-109">Csak az időpontos hálózati hozzáférés házirendjének törlése</span><span class="sxs-lookup"><span data-stu-id="ea6f6-109">Deletes a Just In Time network access policy.</span></span>
<span data-ttu-id="ea6f6-110">Ezt követően a felhasználó nem tud ideiglenes hálózati kapcsolatot kérni a törölt házirenden belül konfigurált VMs-kapcsolaton.</span><span class="sxs-lookup"><span data-stu-id="ea6f6-110">After this action a user will not be able to request temporary network connection on the VMs that were configured inside the deleted policy.</span></span>

## <span data-ttu-id="ea6f6-111">Példák</span><span class="sxs-lookup"><span data-stu-id="ea6f6-111">EXAMPLES</span></span>

### <span data-ttu-id="ea6f6-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ea6f6-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default"
```

<span data-ttu-id="ea6f6-113">Csak az időpontos hálózati hozzáférés házirendjének törlése</span><span class="sxs-lookup"><span data-stu-id="ea6f6-113">Deletes a Just In Time network access policy.</span></span>

## <span data-ttu-id="ea6f6-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ea6f6-114">PARAMETERS</span></span>

### <span data-ttu-id="ea6f6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea6f6-115">-DefaultProfile</span></span>
<span data-ttu-id="ea6f6-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ea6f6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea6f6-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ea6f6-117">-InputObject</span></span>
<span data-ttu-id="ea6f6-118">Beviteli objektum</span><span class="sxs-lookup"><span data-stu-id="ea6f6-118">Input Object.</span></span>

```yaml
Type: PSRemoveJitNetworkAccessPolicy
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ea6f6-119">-Hely</span><span class="sxs-lookup"><span data-stu-id="ea6f6-119">-Location</span></span>
<span data-ttu-id="ea6f6-120">Helyre.</span><span class="sxs-lookup"><span data-stu-id="ea6f6-120">Location.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea6f6-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ea6f6-121">-Name</span></span>
<span data-ttu-id="ea6f6-122">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="ea6f6-122">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea6f6-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ea6f6-123">-PassThru</span></span>
<span data-ttu-id="ea6f6-124">Adja meg, hogy a művelet sikeres volt-e.</span><span class="sxs-lookup"><span data-stu-id="ea6f6-124">Return whether the operation was successful.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea6f6-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea6f6-125">-ResourceGroupName</span></span>
<span data-ttu-id="ea6f6-126">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="ea6f6-126">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea6f6-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ea6f6-127">-ResourceId</span></span>
<span data-ttu-id="ea6f6-128">Erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="ea6f6-128">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea6f6-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ea6f6-129">-Confirm</span></span>
<span data-ttu-id="ea6f6-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ea6f6-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea6f6-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea6f6-131">-WhatIf</span></span>
<span data-ttu-id="ea6f6-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ea6f6-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ea6f6-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ea6f6-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea6f6-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea6f6-134">CommonParameters</span></span>
<span data-ttu-id="ea6f6-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ea6f6-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea6f6-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea6f6-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea6f6-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ea6f6-137">INPUTS</span></span>

### <span data-ttu-id="ea6f6-138">System. String</span><span class="sxs-lookup"><span data-stu-id="ea6f6-138">System.String</span></span>
<span data-ttu-id="ea6f6-139">Microsoft. Azure. Command. Security. parancsmagok. JitNetworkAccessPolicies. PSRemoveJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ea6f6-139">Microsoft.Azure.Commands.Security.Cmdlets.JitNetworkAccessPolicies.PSRemoveJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="ea6f6-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ea6f6-140">OUTPUTS</span></span>

### <span data-ttu-id="ea6f6-141">Microsoft. Azure. commands. Security. models. JitNetworkAccessPolicies. PSSecurityJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ea6f6-141">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="ea6f6-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ea6f6-142">NOTES</span></span>

## <span data-ttu-id="ea6f6-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ea6f6-143">RELATED LINKS</span></span>
