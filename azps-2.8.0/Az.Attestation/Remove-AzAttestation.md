---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/remove-azattestation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Remove-AzAttestation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Remove-AzAttestation.md
ms.openlocfilehash: 997e1150549ac219c54e42fdd4c7674cd53d5ddc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667882"
---
# <span data-ttu-id="1a0be-101">Remove-AzAttestation</span><span class="sxs-lookup"><span data-stu-id="1a0be-101">Remove-AzAttestation</span></span>

## <span data-ttu-id="1a0be-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1a0be-102">SYNOPSIS</span></span>
<span data-ttu-id="1a0be-103">Tanúsítvány törlése</span><span class="sxs-lookup"><span data-stu-id="1a0be-103">Deletes an attestation.</span></span>

## <span data-ttu-id="1a0be-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1a0be-104">SYNTAX</span></span>

### <span data-ttu-id="1a0be-105">ByAvailableAttestation (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1a0be-105">ByAvailableAttestation (Default)</span></span>
```
Remove-AzAttestation [-Name] <String> [-ResourceGroupName] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a0be-106">ResourceIdByAvailableAttestation</span><span class="sxs-lookup"><span data-stu-id="1a0be-106">ResourceIdByAvailableAttestation</span></span>
```
Remove-AzAttestation [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a0be-107">InputObjectByAvailableAttestation</span><span class="sxs-lookup"><span data-stu-id="1a0be-107">InputObjectByAvailableAttestation</span></span>
```
Remove-AzAttestation [-InputObject] <PSAttestation> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1a0be-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="1a0be-108">DESCRIPTION</span></span>
<span data-ttu-id="1a0be-109">A Remove-AzAttestation parancsmag törli a megadott tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="1a0be-109">The Remove-AzAttestation cmdlet deletes the specified attestation.</span></span>

## <span data-ttu-id="1a0be-110">Példák</span><span class="sxs-lookup"><span data-stu-id="1a0be-110">EXAMPLES</span></span>

### <span data-ttu-id="1a0be-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="1a0be-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzAttestation -Name example -ResourceGroupName rg1 
```

<span data-ttu-id="1a0be-112">Tanúsítvány törlése "példa" a jelenlegi előfizetés és erőforráscsoport "rg1".</span><span class="sxs-lookup"><span data-stu-id="1a0be-112">Delete Attestation "example" from current Subscription and Resource Group "rg1".</span></span>

## <span data-ttu-id="1a0be-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1a0be-113">PARAMETERS</span></span>

### <span data-ttu-id="1a0be-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1a0be-114">-AsJob</span></span>
<span data-ttu-id="1a0be-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="1a0be-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1a0be-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a0be-116">-DefaultProfile</span></span>
<span data-ttu-id="1a0be-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1a0be-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1a0be-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1a0be-118">-InputObject</span></span>
<span data-ttu-id="1a0be-119">Törölni kívánt igazolási objektum</span><span class="sxs-lookup"><span data-stu-id="1a0be-119">Attestation object to be deleted.</span></span>

```yaml
Type: PSAttestation
Parameter Sets: InputObjectByAvailableAttestation
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1a0be-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1a0be-120">-Name</span></span>
<span data-ttu-id="1a0be-121">Az eltávolítandó tanúsítvány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1a0be-121">Specifies the name of the attestation to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByAvailableAttestation
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a0be-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1a0be-122">-PassThru</span></span>
<span data-ttu-id="1a0be-123">Ez a parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="1a0be-123">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="1a0be-124">Ha meg van adva ez a kapcsoló, az eredmény igaz, ha sikeres.</span><span class="sxs-lookup"><span data-stu-id="1a0be-124">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="1a0be-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a0be-125">-ResourceGroupName</span></span>
<span data-ttu-id="1a0be-126">Az Azure tanúsítvány eltávolításához használt erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1a0be-126">Specifies the name of resource group for Azure attestation to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByAvailableAttestation
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a0be-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1a0be-127">-ResourceId</span></span>
<span data-ttu-id="1a0be-128">Tanúsítvány-erőforrás azonosítója</span><span class="sxs-lookup"><span data-stu-id="1a0be-128">Attestation Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdByAvailableAttestation
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a0be-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1a0be-129">-Confirm</span></span>
<span data-ttu-id="1a0be-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1a0be-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a0be-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a0be-131">-WhatIf</span></span>
<span data-ttu-id="1a0be-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1a0be-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1a0be-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1a0be-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a0be-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a0be-134">CommonParameters</span></span>
<span data-ttu-id="1a0be-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1a0be-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a0be-136">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="1a0be-136">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a0be-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1a0be-137">INPUTS</span></span>

### <span data-ttu-id="1a0be-138">System. String</span><span class="sxs-lookup"><span data-stu-id="1a0be-138">System.String</span></span>

### <span data-ttu-id="1a0be-139">Microsoft. Azure. commands. igazolás. models. PSAttestation</span><span class="sxs-lookup"><span data-stu-id="1a0be-139">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span></span>

## <span data-ttu-id="1a0be-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1a0be-140">OUTPUTS</span></span>

### <span data-ttu-id="1a0be-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1a0be-141">System.Boolean</span></span>

## <span data-ttu-id="1a0be-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1a0be-142">NOTES</span></span>

## <span data-ttu-id="1a0be-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1a0be-143">RELATED LINKS</span></span>
