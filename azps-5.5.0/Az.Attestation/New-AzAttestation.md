---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/new-azattestation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/New-AzAttestation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/New-AzAttestation.md
ms.openlocfilehash: c9295883035ca7c53742fc9cb6d1b2e9a800eb3f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100162507"
---
# <span data-ttu-id="f8568-101">New-AzAttestation</span><span class="sxs-lookup"><span data-stu-id="f8568-101">New-AzAttestation</span></span>

## <span data-ttu-id="f8568-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f8568-102">SYNOPSIS</span></span>
<span data-ttu-id="f8568-103">Egy igazolást hoz létre</span><span class="sxs-lookup"><span data-stu-id="f8568-103">Creates an attestation</span></span>

## <span data-ttu-id="f8568-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f8568-104">SYNTAX</span></span>

```
New-AzAttestation -Name <String> -ResourceGroupName <String> -Location <String> [-Tag <Hashtable>]
 [-PolicySignersCertificateFile <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f8568-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f8568-105">DESCRIPTION</span></span>
<span data-ttu-id="f8568-106">A New-AzAttestation parancsmag létrehoz egy atteócionálást a megadott erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="f8568-106">The New-AzAttestation cmdlet creates an attestation in the specified resource group.</span></span>

## <span data-ttu-id="f8568-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f8568-107">EXAMPLES</span></span>

### <span data-ttu-id="f8568-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="f8568-108">Example 1</span></span>
```powershell
PS C:\> New-AzAttestation -Name pshtest4 -ResourceGroupName psh-test-rg -Location "East US" -Tags @{Test="true";CreationYear="2020"}                                                                                                                                                                                         
Id                : subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/psh-test-rg/providers/Microsoft.Attestation/attestationProviders/pshtest4
Location          : East US
ResourceGroupName : psh-test-rg
Name              : pshtest4
Status            : Ready
TrustModel        : AAD
AttestUri         : https://pshtest4.us.attest.azure.net
Tags              : {CreationYear, Test}
TagsTable         :
                    Name          Value
                    ============  =====
                    CreationYear  2020
                    Test          true
```

<span data-ttu-id="f8568-109">Hozzon létre egy *pshtest4* nevű szolgáltató új példányát néhány címkével, és használja az AAD-megbízhatóságot a TEE-házirendek elsajátítása érdekében.</span><span class="sxs-lookup"><span data-stu-id="f8568-109">Create a new instance of an Attestation Provider named *pshtest4* with a couple tags and using AAD trust for mastering TEE policy.</span></span>

### <span data-ttu-id="f8568-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="f8568-110">Example 2</span></span>
```powershell
PS C:\> New-AzAttestation -Name pshtest3 -ResourceGroupName psh-test-rg -Location "East US" -PolicySignersCertificateFile .\cert1.pem                                                                                                                                                
Id                : subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/psh-test-rg/providers/Microsoft.Attestation/attestationProviders/pshtest3
Location          : East US
ResourceGroupName : psh-test-rg
Name              : pshtest3
Status            : Ready
TrustModel        : Isolated
AttestUri         : https://pshtest3.us.attest.azure.net
Tags              :
TagsTable         :
```

<span data-ttu-id="f8568-111">Hozzon létre egy *pshtest3* nevű tanúsítványszolgáltató új példányát, amely az Isoladed trust használatával elsajátítja a TEE-házirendet egy PEM-fájlon keresztüli megbízható aláíró kulcsok készletének megadásával.</span><span class="sxs-lookup"><span data-stu-id="f8568-111">Create a new instance of an Attestation Provider named *pshtest3*\` that uses Isoladed trust for mastering TEE policy via specifying a set of trusted signing keys via a PEM file.</span></span>

## <span data-ttu-id="f8568-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f8568-112">PARAMETERS</span></span>

### <span data-ttu-id="f8568-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8568-113">-DefaultProfile</span></span>
<span data-ttu-id="f8568-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f8568-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f8568-115">-Location</span><span class="sxs-lookup"><span data-stu-id="f8568-115">-Location</span></span>
<span data-ttu-id="f8568-116">Megadja azt az Azure-régiót, amelyben létre kell hoznia a szolgáltatót.</span><span class="sxs-lookup"><span data-stu-id="f8568-116">Specifies the Azure region in which to create the attestation provider.</span></span> <span data-ttu-id="f8568-117">A választható lehetőségek Get-AzResourceProvider a ProviderNamespace paraméterrel megadott parancsokkal.</span><span class="sxs-lookup"><span data-stu-id="f8568-117">Use the command Get-AzResourceProvider with the ProviderNamespace parameter to see your choices.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8568-118">-Name</span><span class="sxs-lookup"><span data-stu-id="f8568-118">-Name</span></span>
<span data-ttu-id="f8568-119">A létrehozni szükséges példány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f8568-119">Specifies a name of the Instance to create.</span></span>
<span data-ttu-id="f8568-120">A név betűk, számjegyek vagy kötőjelek bármilyen kombinációja lehet.</span><span class="sxs-lookup"><span data-stu-id="f8568-120">The name can be any combination of letters, digits, or hyphens.</span></span>
<span data-ttu-id="f8568-121">A névnek betűvel vagy számjegysel kell kezdődnie és végződnie.</span><span class="sxs-lookup"><span data-stu-id="f8568-121">The name must start and end with a letter or digit.</span></span>
<span data-ttu-id="f8568-122">A névnek univerzálisan egyedinek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="f8568-122">The name must be universally unique.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: InstanceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8568-123">-PolicySignersCertificateFile</span><span class="sxs-lookup"><span data-stu-id="f8568-123">-PolicySignersCertificateFile</span></span>
<span data-ttu-id="f8568-124">Egyetlen tanúsítványfájlban adja meg a megbízható aláíró kulcsok halmazát a kibocsátási házirendhez.</span><span class="sxs-lookup"><span data-stu-id="f8568-124">Specifies the set of trusted signing keys for issuance policy in a single certificate file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8568-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8568-125">-ResourceGroupName</span></span>
<span data-ttu-id="f8568-126">Annak a meglévő erőforráscsoportnak a nevét adja meg, amelyben létre kell hoznia a igazolást.</span><span class="sxs-lookup"><span data-stu-id="f8568-126">Specifies the name of an existing resource group in which to create the attestation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8568-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="f8568-127">-Tag</span></span>
<span data-ttu-id="f8568-128">A hash table which represents resource tags.</span><span class="sxs-lookup"><span data-stu-id="f8568-128">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8568-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f8568-129">-Confirm</span></span>
<span data-ttu-id="f8568-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="f8568-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8568-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8568-131">-WhatIf</span></span>
<span data-ttu-id="f8568-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="f8568-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8568-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f8568-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8568-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8568-134">CommonParameters</span></span>
<span data-ttu-id="f8568-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8568-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8568-136">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f8568-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8568-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f8568-137">INPUTS</span></span>

### <span data-ttu-id="f8568-138">System.String</span><span class="sxs-lookup"><span data-stu-id="f8568-138">System.String</span></span>

### <span data-ttu-id="f8568-139">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="f8568-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="f8568-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f8568-140">OUTPUTS</span></span>

### <span data-ttu-id="f8568-141">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span><span class="sxs-lookup"><span data-stu-id="f8568-141">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span></span>

## <span data-ttu-id="f8568-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f8568-142">NOTES</span></span>

## <span data-ttu-id="f8568-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f8568-143">RELATED LINKS</span></span>
