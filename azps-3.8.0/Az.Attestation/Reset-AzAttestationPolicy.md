---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/reset-azattestationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Reset-AzAttestationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Reset-AzAttestationPolicy.md
ms.openlocfilehash: a2b8d83254c84ee974173611912dd9b21cb7a26d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012726"
---
# <span data-ttu-id="8e538-101">Reset-AzAttestationPolicy</span><span class="sxs-lookup"><span data-stu-id="8e538-101">Reset-AzAttestationPolicy</span></span>

## <span data-ttu-id="8e538-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8e538-102">SYNOPSIS</span></span>
<span data-ttu-id="8e538-103">Visszaállítja a házirendet egy bérlői webhelyről az Azure Attestationn.}</span><span class="sxs-lookup"><span data-stu-id="8e538-103">Resets the policy from a tenant in Azure Attestationn.}</span></span>

## <span data-ttu-id="8e538-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8e538-104">SYNTAX</span></span>

### <span data-ttu-id="8e538-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e538-105">NameParameterSet</span></span>
```
Reset-AzAttestationPolicy [-Name] <String> [-ResourceGroupName] <String> -Tee <String> [-Policy <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e538-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e538-106">ResourceIdParameterSet</span></span>
```
Reset-AzAttestationPolicy [-ResourceId] <String> -Tee <String> [-Policy <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e538-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="8e538-107">DESCRIPTION</span></span>
<span data-ttu-id="8e538-108">Az Reset-AzAttestationPolicy parancsmag visszaállítja a felhasználó által definiált tanúsítvány-házirendet az Azure tanúsítványban szereplő bérlői webhelyre.</span><span class="sxs-lookup"><span data-stu-id="8e538-108">The Reset-AzAttestationPolicy cmdlet resets the user defined attestation policy from a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="8e538-109">Példák</span><span class="sxs-lookup"><span data-stu-id="8e538-109">EXAMPLES</span></span>

### <span data-ttu-id="8e538-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="8e538-110">Example 1</span></span>
```powershell
PS C:\> Reset-AzAttestationPolicy -Name pshtest -ResourceGroupName psh-test-rg -Tee SgxEnclave
```

<span data-ttu-id="8e538-111">Állítsa alaphelyzetbe a házirendet az alapértelmezett értékre a Tee Type *SgxEnclave* hitelesítő szolgáltató *pshtest* .</span><span class="sxs-lookup"><span data-stu-id="8e538-111">Reset the policy to the default for the Attestation Provider *pshtest* for Tee type *SgxEnclave*.</span></span>

## <span data-ttu-id="8e538-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8e538-112">PARAMETERS</span></span>

### <span data-ttu-id="8e538-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e538-113">-DefaultProfile</span></span>
<span data-ttu-id="8e538-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8e538-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e538-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8e538-115">-Name</span></span>
<span data-ttu-id="8e538-116">A bérlő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8e538-116">Specifies a name of the tenant.</span></span>
<span data-ttu-id="8e538-117">Ez a parancsmag visszaállítja a bérlő által a paraméter által megadott tanúsítvány-házirendet.</span><span class="sxs-lookup"><span data-stu-id="8e538-117">This cmdlet resets the attestation policy for the tenant that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e538-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8e538-118">-PassThru</span></span>
<span data-ttu-id="8e538-119">Ez a parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="8e538-119">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="8e538-120">Ha meg van adva ez a kapcsoló, az eredmény igaz, ha sikeres.</span><span class="sxs-lookup"><span data-stu-id="8e538-120">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="8e538-121">-Házirend</span><span class="sxs-lookup"><span data-stu-id="8e538-121">-Policy</span></span>
<span data-ttu-id="8e538-122">Azt a JSON-webtokent adja meg, amely leírja az alaphelyzetbe állított házirend-dokumentumot.</span><span class="sxs-lookup"><span data-stu-id="8e538-122">Specifies the JSON Web Token describing the policy document to reset.</span></span>

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

### <span data-ttu-id="8e538-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e538-123">-ResourceGroupName</span></span>
<span data-ttu-id="8e538-124">A tanúsítvány-szolgáltató erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8e538-124">Specifies the resource group name of an attestation provider.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e538-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8e538-125">-ResourceId</span></span>
<span data-ttu-id="8e538-126">A hitelesítő szolgáltató ResourceID adja meg.</span><span class="sxs-lookup"><span data-stu-id="8e538-126">Specifies the ResourceID of an attestation provider.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e538-127">-Tee</span><span class="sxs-lookup"><span data-stu-id="8e538-127">-Tee</span></span>
<span data-ttu-id="8e538-128">A megbízható végrehajtási környezet típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="8e538-128">Specifies a type of Trusted Execution Environment.</span></span>
<span data-ttu-id="8e538-129">Négy típusú környezetet támogatunk: SgxEnclave, OpenEnclave, CyResComponent és VBSEnclave.</span><span class="sxs-lookup"><span data-stu-id="8e538-129">We support four types of environment: SgxEnclave, OpenEnclave, CyResComponent and VBSEnclave.</span></span>

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

### <span data-ttu-id="8e538-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8e538-130">-Confirm</span></span>
<span data-ttu-id="8e538-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8e538-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e538-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e538-132">-WhatIf</span></span>
<span data-ttu-id="8e538-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8e538-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e538-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8e538-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e538-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e538-135">CommonParameters</span></span>
<span data-ttu-id="8e538-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8e538-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e538-137">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="8e538-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e538-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8e538-138">INPUTS</span></span>

### <span data-ttu-id="8e538-139">System. String</span><span class="sxs-lookup"><span data-stu-id="8e538-139">System.String</span></span>

## <span data-ttu-id="8e538-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8e538-140">OUTPUTS</span></span>

### <span data-ttu-id="8e538-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8e538-141">System.Boolean</span></span>

## <span data-ttu-id="8e538-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8e538-142">NOTES</span></span>

## <span data-ttu-id="8e538-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8e538-143">RELATED LINKS</span></span>
