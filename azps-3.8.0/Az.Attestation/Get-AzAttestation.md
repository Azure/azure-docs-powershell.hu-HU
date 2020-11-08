---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/get-azattestation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Get-AzAttestation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Get-AzAttestation.md
ms.openlocfilehash: a18222c40dc5c56bd2d67afb8d0df35b7aedc532
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012740"
---
# <span data-ttu-id="b2776-101">Get-AzAttestation</span><span class="sxs-lookup"><span data-stu-id="b2776-101">Get-AzAttestation</span></span>

## <span data-ttu-id="b2776-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b2776-102">SYNOPSIS</span></span>
<span data-ttu-id="b2776-103">Igazolást kap.</span><span class="sxs-lookup"><span data-stu-id="b2776-103">Gets an attestation.</span></span>

## <span data-ttu-id="b2776-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b2776-104">SYNTAX</span></span>

### <span data-ttu-id="b2776-105">NameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b2776-105">NameParameterSet (Default)</span></span>
```
Get-AzAttestation [-Name] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b2776-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b2776-106">ResourceIdParameterSet</span></span>
```
Get-AzAttestation [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b2776-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="b2776-107">DESCRIPTION</span></span>
<span data-ttu-id="b2776-108">Az Get-AzAttestation parancsmag információt kap az előfizetésben szereplő tanúsítványról.</span><span class="sxs-lookup"><span data-stu-id="b2776-108">The Get-AzAttestation cmdlet gets information about the attestation in a subscription.</span></span>

## <span data-ttu-id="b2776-109">Példák</span><span class="sxs-lookup"><span data-stu-id="b2776-109">EXAMPLES</span></span>

### <span data-ttu-id="b2776-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="b2776-110">Example 1</span></span>
```powershell
PS C:\> Get-AzAttestation -Name pshtest -ResourceGroupName psh-test-rg                                                                                                                                                                                                                                                       
Id                : subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/psh-test-rg/providers/Microsoft.Attestation/attestationProviders/pshtest
Location          : East US
ResourceGroupName : psh-test-rg
Name              : pshtest
Status            : Ready
TrustModel        : AAD
AttestUri         : https://pshtest.us.attest.azure.net
Tags              : {Production, Example}
TagsTable         :
                    Name        Value
                    ==========  =====
                    Production  False
                    Example     True
```

<span data-ttu-id="b2776-111">Hitelesítő szolgáltató *pshtest* az erőforráscsoport *PSH – teszt – RG*.</span><span class="sxs-lookup"><span data-stu-id="b2776-111">Get Attestation Provider *pshtest* in Resource Group *psh-test-rg*.</span></span>

## <span data-ttu-id="b2776-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b2776-112">PARAMETERS</span></span>

### <span data-ttu-id="b2776-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2776-113">-DefaultProfile</span></span>
<span data-ttu-id="b2776-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b2776-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b2776-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b2776-115">-Name</span></span>
<span data-ttu-id="b2776-116">Tanúsítvány neve.</span><span class="sxs-lookup"><span data-stu-id="b2776-116">Attestation Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2776-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2776-117">-ResourceGroupName</span></span>
<span data-ttu-id="b2776-118">A lekérdezett tanúsítványhoz tartozó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b2776-118">Specifies the name of the resource group associated with the attestation being queried.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2776-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b2776-119">-ResourceId</span></span>
<span data-ttu-id="b2776-120">A lekérdezett tanúsítvánnyal társított ResourceID nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b2776-120">Specifies the name of the ResourceID associated with the attestation being queried</span></span>

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

### <span data-ttu-id="b2776-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2776-121">CommonParameters</span></span>
<span data-ttu-id="b2776-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b2776-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2776-123">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b2776-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2776-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b2776-124">INPUTS</span></span>

### <span data-ttu-id="b2776-125">System. String</span><span class="sxs-lookup"><span data-stu-id="b2776-125">System.String</span></span>

## <span data-ttu-id="b2776-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b2776-126">OUTPUTS</span></span>

### <span data-ttu-id="b2776-127">Microsoft. Azure. commands. igazolás. models. PSAttestation</span><span class="sxs-lookup"><span data-stu-id="b2776-127">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span></span>

## <span data-ttu-id="b2776-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b2776-128">NOTES</span></span>

## <span data-ttu-id="b2776-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b2776-129">RELATED LINKS</span></span>
