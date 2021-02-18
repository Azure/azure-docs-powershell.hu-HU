---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azsecuritypartnerprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzSecurityPartnerProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzSecurityPartnerProvider.md
ms.openlocfilehash: a51345653580261178191687f54bf0f2a8cc6f0c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202514"
---
# <span data-ttu-id="44329-101">Remove-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="44329-101">Remove-AzSecurityPartnerProvider</span></span>

## <span data-ttu-id="44329-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="44329-102">SYNOPSIS</span></span>
<span data-ttu-id="44329-103">Egy Azure SecurityPartnerProvider törlése.</span><span class="sxs-lookup"><span data-stu-id="44329-103">Deletes an Azure SecurityPartnerProvider.</span></span>

## <span data-ttu-id="44329-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="44329-104">SYNTAX</span></span>

### <span data-ttu-id="44329-105">SecurityPartnerProviderNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="44329-105">SecurityPartnerProviderNameParameterSet</span></span>
```
Remove-AzSecurityPartnerProvider -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44329-106">SecurityPartnerProviderInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="44329-106">SecurityPartnerProviderInputObjectParameterSet</span></span>
```
Remove-AzSecurityPartnerProvider -SecurityPartnerProvider <PSSecurityPartnerProvider> [-Force] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44329-107">SecurityPartnerProviderResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="44329-107">SecurityPartnerProviderResourceIdParameterSet</span></span>
```
Remove-AzSecurityPartnerProvider -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="44329-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="44329-108">DESCRIPTION</span></span>
<span data-ttu-id="44329-109">A **Remove-AzSecurityPartnerProvider** parancsmag töröl egy Azure SecurityPartnerProvider-t</span><span class="sxs-lookup"><span data-stu-id="44329-109">The **Remove-AzSecurityPartnerProvider** cmdlet deletes an Azure SecurityPartnerProvider</span></span>

## <span data-ttu-id="44329-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="44329-110">EXAMPLES</span></span>

### <span data-ttu-id="44329-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="44329-111">Example 1</span></span>
```powershell
Remove-AzSecurityPartnerProvider -ResourceGroupName securityPartnerProviderRG -Name securityPartnerProvider
```

## <span data-ttu-id="44329-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="44329-112">PARAMETERS</span></span>

### <span data-ttu-id="44329-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="44329-113">-AsJob</span></span>
<span data-ttu-id="44329-114">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="44329-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="44329-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44329-115">-DefaultProfile</span></span>
<span data-ttu-id="44329-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="44329-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44329-117">-Force</span><span class="sxs-lookup"><span data-stu-id="44329-117">-Force</span></span>
<span data-ttu-id="44329-118">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="44329-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="44329-119">-Name</span><span class="sxs-lookup"><span data-stu-id="44329-119">-Name</span></span>
<span data-ttu-id="44329-120">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="44329-120">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SecurityPartnerProviderNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44329-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="44329-121">-PassThru</span></span>
<span data-ttu-id="44329-122">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amelyen a műveletet végre kell hajtotta.</span><span class="sxs-lookup"><span data-stu-id="44329-122">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="44329-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44329-123">-ResourceGroupName</span></span>
<span data-ttu-id="44329-124">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="44329-124">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: SecurityPartnerProviderNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44329-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="44329-125">-ResourceId</span></span>
<span data-ttu-id="44329-126">The securityPartnerProvider resource Id.</span><span class="sxs-lookup"><span data-stu-id="44329-126">The securityPartnerProvider resource Id.</span></span>

```yaml
Type: String
Parameter Sets: SecurityPartnerProviderResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44329-127">-SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="44329-127">-SecurityPartnerProvider</span></span>
<span data-ttu-id="44329-128">The securityPartnerProvider input object.</span><span class="sxs-lookup"><span data-stu-id="44329-128">The securityPartnerProvider input object.</span></span>

```yaml
Type: PSSecurityPartnerProvider
Parameter Sets: SecurityPartnerProviderInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="44329-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="44329-129">-Confirm</span></span>
<span data-ttu-id="44329-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="44329-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44329-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44329-131">-WhatIf</span></span>
<span data-ttu-id="44329-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="44329-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44329-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="44329-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44329-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44329-134">CommonParameters</span></span>
<span data-ttu-id="44329-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44329-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44329-136">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="44329-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44329-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="44329-137">INPUTS</span></span>

### <span data-ttu-id="44329-138">System.String</span><span class="sxs-lookup"><span data-stu-id="44329-138">System.String</span></span>

### <span data-ttu-id="44329-139">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="44329-139">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span></span>

## <span data-ttu-id="44329-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="44329-140">OUTPUTS</span></span>

### <span data-ttu-id="44329-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="44329-141">System.Boolean</span></span>

## <span data-ttu-id="44329-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="44329-142">NOTES</span></span>

## <span data-ttu-id="44329-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="44329-143">RELATED LINKS</span></span>
