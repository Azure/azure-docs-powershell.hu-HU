---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/remove-azattestation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Remove-AzAttestation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Remove-AzAttestation.md
ms.openlocfilehash: 16e728443e228a2a9b85806caf8cf55ec9c115c3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299846"
---
# <span data-ttu-id="6630b-101">Remove-AzAttestation</span><span class="sxs-lookup"><span data-stu-id="6630b-101">Remove-AzAttestation</span></span>

## <span data-ttu-id="6630b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6630b-102">SYNOPSIS</span></span>
<span data-ttu-id="6630b-103">Tanúsítvány törlése</span><span class="sxs-lookup"><span data-stu-id="6630b-103">Deletes an attestation.</span></span>

## <span data-ttu-id="6630b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6630b-104">SYNTAX</span></span>

### <span data-ttu-id="6630b-105">ByAvailableAttestation (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6630b-105">ByAvailableAttestation (Default)</span></span>
```
Remove-AzAttestation [-Name] <String> [-ResourceGroupName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6630b-106">ResourceIdByAvailableAttestation</span><span class="sxs-lookup"><span data-stu-id="6630b-106">ResourceIdByAvailableAttestation</span></span>
```
Remove-AzAttestation [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6630b-107">InputObjectByAvailableAttestation</span><span class="sxs-lookup"><span data-stu-id="6630b-107">InputObjectByAvailableAttestation</span></span>
```
Remove-AzAttestation [-InputObject] <PSAttestation> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6630b-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="6630b-108">DESCRIPTION</span></span>
<span data-ttu-id="6630b-109">A Remove-AzAttestation parancsmag törli a megadott tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="6630b-109">The Remove-AzAttestation cmdlet deletes the specified attestation.</span></span>

## <span data-ttu-id="6630b-110">Példák</span><span class="sxs-lookup"><span data-stu-id="6630b-110">EXAMPLES</span></span>

### <span data-ttu-id="6630b-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="6630b-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzAttestation -Name pshtest3 -ResourceGroupName psh-test-rg
```

<span data-ttu-id="6630b-112">Törölje a *pshtest3* nevű tanúsítvány-szolgáltatót az aktuális előfizetésből a *PSH-teszt-RG* nevű erőforráscsoport nevű erőforrás csoportban.</span><span class="sxs-lookup"><span data-stu-id="6630b-112">Delete the Attestation Provider named *pshtest3* in the resource group named *psh-test-rg* from the current subscription.</span></span>

## <span data-ttu-id="6630b-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6630b-113">PARAMETERS</span></span>

### <span data-ttu-id="6630b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6630b-114">-DefaultProfile</span></span>
<span data-ttu-id="6630b-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6630b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6630b-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6630b-116">-InputObject</span></span>
<span data-ttu-id="6630b-117">Törölni kívánt igazolási objektum</span><span class="sxs-lookup"><span data-stu-id="6630b-117">Attestation object to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Attestation.Models.PSAttestation
Parameter Sets: InputObjectByAvailableAttestation
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6630b-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6630b-118">-Name</span></span>
<span data-ttu-id="6630b-119">Az eltávolítandó tanúsítvány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6630b-119">Specifies the name of the attestation to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAvailableAttestation
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6630b-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6630b-120">-PassThru</span></span>
<span data-ttu-id="6630b-121">Ez a parancsmag alapértelmezés szerint nem ad vissza objektumot.</span><span class="sxs-lookup"><span data-stu-id="6630b-121">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="6630b-122">Ha meg van adva ez a kapcsoló, az eredmény igaz, ha sikeres.</span><span class="sxs-lookup"><span data-stu-id="6630b-122">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="6630b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6630b-123">-ResourceGroupName</span></span>
<span data-ttu-id="6630b-124">Az Azure tanúsítvány eltávolításához használt erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6630b-124">Specifies the name of resource group for Azure attestation to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAvailableAttestation
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6630b-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6630b-125">-ResourceId</span></span>
<span data-ttu-id="6630b-126">Tanúsítvány-erőforrás azonosítója</span><span class="sxs-lookup"><span data-stu-id="6630b-126">Attestation Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdByAvailableAttestation
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6630b-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6630b-127">-Confirm</span></span>
<span data-ttu-id="6630b-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6630b-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6630b-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6630b-129">-WhatIf</span></span>
<span data-ttu-id="6630b-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6630b-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6630b-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6630b-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6630b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6630b-132">CommonParameters</span></span>
<span data-ttu-id="6630b-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6630b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6630b-134">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="6630b-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6630b-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6630b-135">INPUTS</span></span>

### <span data-ttu-id="6630b-136">System. String</span><span class="sxs-lookup"><span data-stu-id="6630b-136">System.String</span></span>

### <span data-ttu-id="6630b-137">Microsoft. Azure. commands. igazolás. models. PSAttestation</span><span class="sxs-lookup"><span data-stu-id="6630b-137">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span></span>

## <span data-ttu-id="6630b-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6630b-138">OUTPUTS</span></span>

### <span data-ttu-id="6630b-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6630b-139">System.Boolean</span></span>

## <span data-ttu-id="6630b-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6630b-140">NOTES</span></span>

## <span data-ttu-id="6630b-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6630b-141">RELATED LINKS</span></span>
