---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/new-azattestation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/New-AzAttestation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/New-AzAttestation.md
ms.openlocfilehash: ce21b116ceb41bfdfb26008dd44c914f3198ab39
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667883"
---
# <span data-ttu-id="2ff36-101">New-AzAttestation</span><span class="sxs-lookup"><span data-stu-id="2ff36-101">New-AzAttestation</span></span>

## <span data-ttu-id="2ff36-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2ff36-102">SYNOPSIS</span></span>
<span data-ttu-id="2ff36-103">Tanúsítvány létrehozása</span><span class="sxs-lookup"><span data-stu-id="2ff36-103">Creates an attestation</span></span>

## <span data-ttu-id="2ff36-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2ff36-104">SYNTAX</span></span>

```
New-AzAttestation -Name <String> -ResourceGroupName <String> [-AttestationPolicy <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ff36-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2ff36-105">DESCRIPTION</span></span>
<span data-ttu-id="2ff36-106">Az New-AzAttestation parancsmag a megadott erőforráscsoport tanúsítványát hozza létre.</span><span class="sxs-lookup"><span data-stu-id="2ff36-106">The New-AzAttestation cmdlet creates an attestation in the specified resource group.</span></span>

## <span data-ttu-id="2ff36-107">Példák</span><span class="sxs-lookup"><span data-stu-id="2ff36-107">EXAMPLES</span></span>

### <span data-ttu-id="2ff36-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="2ff36-108">Example 1</span></span>
```powershell
PS C:\> New-AzAttestation -Name example -ResourceGroupName rg1 
Id                  : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/rg1/providers/Microsoft.Attestation/attestationProviders/example
Name                : example
Type                : Microsoft.Attestation/attestationProviders
Status              : Ready
AttesUri            : https://example.us.attest.azure.net
ResoureGroupName    : rg1 
SubscriptionId      : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
```

<span data-ttu-id="2ff36-109">Új tanúsítvány létrehozása "példa" a jelenlegi előfizetésben, erőforráscsoport "rg1"</span><span class="sxs-lookup"><span data-stu-id="2ff36-109">Create a new Attestation "example" in current Subscription, Resource Group "rg1"</span></span>

## <span data-ttu-id="2ff36-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2ff36-110">PARAMETERS</span></span>

### <span data-ttu-id="2ff36-111">-AttestationPolicy</span><span class="sxs-lookup"><span data-stu-id="2ff36-111">-AttestationPolicy</span></span>
<span data-ttu-id="2ff36-112">Itt adhatja meg azt a tanúsítvány-házirendet, amelybe az igazolást létre kívánja hozni.</span><span class="sxs-lookup"><span data-stu-id="2ff36-112">Specifies the attestation policy passed in which to create the attestation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ff36-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ff36-113">-DefaultProfile</span></span>
<span data-ttu-id="2ff36-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2ff36-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ff36-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2ff36-115">-Name</span></span>
<span data-ttu-id="2ff36-116">A létrehozandó példány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2ff36-116">Specifies a name of the Instance to create.</span></span>
<span data-ttu-id="2ff36-117">A név lehet betűk, számjegyek és kötőjelek tetszőleges kombinációja.</span><span class="sxs-lookup"><span data-stu-id="2ff36-117">The name can be any combination of letters, digits, or hyphens.</span></span>
<span data-ttu-id="2ff36-118">A névnek betűvel vagy számmal kell kezdődnie.</span><span class="sxs-lookup"><span data-stu-id="2ff36-118">The name must start and end with a letter or digit.</span></span>
<span data-ttu-id="2ff36-119">A névnek univerzálisan egyedinek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="2ff36-119">The name must be universally unique.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: InstanceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ff36-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ff36-120">-ResourceGroupName</span></span>
<span data-ttu-id="2ff36-121">Annak a csoportnak a nevét adja meg, amelybe az igazolást létre szeretné hozni.</span><span class="sxs-lookup"><span data-stu-id="2ff36-121">Specifies the name of an existing resource group in which to create the attestation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ff36-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2ff36-122">-Confirm</span></span>
<span data-ttu-id="2ff36-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2ff36-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ff36-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ff36-124">-WhatIf</span></span>
<span data-ttu-id="2ff36-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2ff36-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ff36-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2ff36-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ff36-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ff36-127">CommonParameters</span></span>
<span data-ttu-id="2ff36-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2ff36-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ff36-129">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="2ff36-129">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ff36-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2ff36-130">INPUTS</span></span>

### <span data-ttu-id="2ff36-131">System. String</span><span class="sxs-lookup"><span data-stu-id="2ff36-131">System.String</span></span>

## <span data-ttu-id="2ff36-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2ff36-132">OUTPUTS</span></span>

### <span data-ttu-id="2ff36-133">Microsoft. Azure. commands. igazolás. models. PSAttestation</span><span class="sxs-lookup"><span data-stu-id="2ff36-133">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span></span>

## <span data-ttu-id="2ff36-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2ff36-134">NOTES</span></span>

## <span data-ttu-id="2ff36-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2ff36-135">RELATED LINKS</span></span>
