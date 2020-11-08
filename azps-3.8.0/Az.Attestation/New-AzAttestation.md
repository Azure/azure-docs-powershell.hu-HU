---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/new-azattestation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/New-AzAttestation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/New-AzAttestation.md
ms.openlocfilehash: c9295883035ca7c53742fc9cb6d1b2e9a800eb3f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012738"
---
# <span data-ttu-id="7ff51-101">New-AzAttestation</span><span class="sxs-lookup"><span data-stu-id="7ff51-101">New-AzAttestation</span></span>

## <span data-ttu-id="7ff51-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7ff51-102">SYNOPSIS</span></span>
<span data-ttu-id="7ff51-103">Tanúsítvány létrehozása</span><span class="sxs-lookup"><span data-stu-id="7ff51-103">Creates an attestation</span></span>

## <span data-ttu-id="7ff51-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7ff51-104">SYNTAX</span></span>

```
New-AzAttestation -Name <String> -ResourceGroupName <String> -Location <String> [-Tag <Hashtable>]
 [-PolicySignersCertificateFile <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7ff51-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7ff51-105">DESCRIPTION</span></span>
<span data-ttu-id="7ff51-106">Az New-AzAttestation parancsmag a megadott erőforráscsoport tanúsítványát hozza létre.</span><span class="sxs-lookup"><span data-stu-id="7ff51-106">The New-AzAttestation cmdlet creates an attestation in the specified resource group.</span></span>

## <span data-ttu-id="7ff51-107">Példák</span><span class="sxs-lookup"><span data-stu-id="7ff51-107">EXAMPLES</span></span>

### <span data-ttu-id="7ff51-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="7ff51-108">Example 1</span></span>
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

<span data-ttu-id="7ff51-109">Hozzon létre egy *pshtest4* nevű tanúsítvány-szolgáltató új példányát egy pár címkével, és használja a aad Trust for mastering Tee Policy szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="7ff51-109">Create a new instance of an Attestation Provider named *pshtest4* with a couple tags and using AAD trust for mastering TEE policy.</span></span>

### <span data-ttu-id="7ff51-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="7ff51-110">Example 2</span></span>
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

<span data-ttu-id="7ff51-111">Hozzon létre egy " *pshtest3* " nevű tanúsítvány-szolgáltató új példányát, amely a Isoladed megbízhatóságát használja a kisajátított Tee-házirendhez, a megbízható aláírási kulcsok halmazának megadásával egy PEM-fájlon keresztül.</span><span class="sxs-lookup"><span data-stu-id="7ff51-111">Create a new instance of an Attestation Provider named *pshtest3* \` that uses Isoladed trust for mastering TEE policy via specifying a set of trusted signing keys via a PEM file.</span></span>

## <span data-ttu-id="7ff51-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7ff51-112">PARAMETERS</span></span>

### <span data-ttu-id="7ff51-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ff51-113">-DefaultProfile</span></span>
<span data-ttu-id="7ff51-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7ff51-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7ff51-115">-Hely</span><span class="sxs-lookup"><span data-stu-id="7ff51-115">-Location</span></span>
<span data-ttu-id="7ff51-116">Azt az Azure-területet adja meg, amelybe a tanúsítvány-szolgáltatót létre kívánja hozni.</span><span class="sxs-lookup"><span data-stu-id="7ff51-116">Specifies the Azure region in which to create the attestation provider.</span></span> <span data-ttu-id="7ff51-117">A ProviderNamespace paraméterrel Get-AzResourceProvider paranccsal megtekintheti a kívánt beállításokat.</span><span class="sxs-lookup"><span data-stu-id="7ff51-117">Use the command Get-AzResourceProvider with the ProviderNamespace parameter to see your choices.</span></span>

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

### <span data-ttu-id="7ff51-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7ff51-118">-Name</span></span>
<span data-ttu-id="7ff51-119">A létrehozandó példány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7ff51-119">Specifies a name of the Instance to create.</span></span>
<span data-ttu-id="7ff51-120">A név lehet betűk, számjegyek és kötőjelek tetszőleges kombinációja.</span><span class="sxs-lookup"><span data-stu-id="7ff51-120">The name can be any combination of letters, digits, or hyphens.</span></span>
<span data-ttu-id="7ff51-121">A névnek betűvel vagy számmal kell kezdődnie.</span><span class="sxs-lookup"><span data-stu-id="7ff51-121">The name must start and end with a letter or digit.</span></span>
<span data-ttu-id="7ff51-122">A névnek univerzálisan egyedinek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="7ff51-122">The name must be universally unique.</span></span>

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

### <span data-ttu-id="7ff51-123">-PolicySignersCertificateFile</span><span class="sxs-lookup"><span data-stu-id="7ff51-123">-PolicySignersCertificateFile</span></span>
<span data-ttu-id="7ff51-124">A kibocsátási házirendhez tartozó megbízható aláírási kulcsok halmazát adja meg egyetlen tanúsítványfájl esetén.</span><span class="sxs-lookup"><span data-stu-id="7ff51-124">Specifies the set of trusted signing keys for issuance policy in a single certificate file.</span></span>

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

### <span data-ttu-id="7ff51-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ff51-125">-ResourceGroupName</span></span>
<span data-ttu-id="7ff51-126">Annak a csoportnak a nevét adja meg, amelybe az igazolást létre szeretné hozni.</span><span class="sxs-lookup"><span data-stu-id="7ff51-126">Specifies the name of an existing resource group in which to create the attestation.</span></span>

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

### <span data-ttu-id="7ff51-127">-Címke</span><span class="sxs-lookup"><span data-stu-id="7ff51-127">-Tag</span></span>
<span data-ttu-id="7ff51-128">Egy kivonatoló táblázat, amely az erőforrás címkéit jelöli.</span><span class="sxs-lookup"><span data-stu-id="7ff51-128">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="7ff51-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7ff51-129">-Confirm</span></span>
<span data-ttu-id="7ff51-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7ff51-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ff51-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ff51-131">-WhatIf</span></span>
<span data-ttu-id="7ff51-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7ff51-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ff51-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7ff51-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ff51-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ff51-134">CommonParameters</span></span>
<span data-ttu-id="7ff51-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7ff51-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ff51-136">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="7ff51-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ff51-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7ff51-137">INPUTS</span></span>

### <span data-ttu-id="7ff51-138">System. String</span><span class="sxs-lookup"><span data-stu-id="7ff51-138">System.String</span></span>

### <span data-ttu-id="7ff51-139">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="7ff51-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="7ff51-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7ff51-140">OUTPUTS</span></span>

### <span data-ttu-id="7ff51-141">Microsoft. Azure. commands. igazolás. models. PSAttestation</span><span class="sxs-lookup"><span data-stu-id="7ff51-141">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span></span>

## <span data-ttu-id="7ff51-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7ff51-142">NOTES</span></span>

## <span data-ttu-id="7ff51-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7ff51-143">RELATED LINKS</span></span>
