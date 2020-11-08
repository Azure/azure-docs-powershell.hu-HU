---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/get-azattestation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Get-AzAttestation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Get-AzAttestation.md
ms.openlocfilehash: 650ac7c478f1c27ca3ba925c4d767f02c79fa781
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94180645"
---
# <span data-ttu-id="05228-101">Get-AzAttestation</span><span class="sxs-lookup"><span data-stu-id="05228-101">Get-AzAttestation</span></span>

## <span data-ttu-id="05228-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="05228-102">SYNOPSIS</span></span>
<span data-ttu-id="05228-103">Igazolást kap.</span><span class="sxs-lookup"><span data-stu-id="05228-103">Gets an attestation.</span></span>

## <span data-ttu-id="05228-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="05228-104">SYNTAX</span></span>

### <span data-ttu-id="05228-105">NameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="05228-105">NameParameterSet (Default)</span></span>
```
Get-AzAttestation [-Name] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="05228-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="05228-106">ResourceIdParameterSet</span></span>
```
Get-AzAttestation [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="05228-107">DefaultProviderParameterSet</span><span class="sxs-lookup"><span data-stu-id="05228-107">DefaultProviderParameterSet</span></span>
```
Get-AzAttestation [[-Location] <String>] [-DefaultProvider] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="05228-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="05228-108">DESCRIPTION</span></span>
<span data-ttu-id="05228-109">Az Get-AzAttestation parancsmag információt kap az előfizetésben szereplő tanúsítványról.</span><span class="sxs-lookup"><span data-stu-id="05228-109">The Get-AzAttestation cmdlet gets information about the attestation in a subscription.</span></span>

## <span data-ttu-id="05228-110">Példák</span><span class="sxs-lookup"><span data-stu-id="05228-110">EXAMPLES</span></span>

### <span data-ttu-id="05228-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="05228-111">Example 1</span></span>
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

<span data-ttu-id="05228-112">Hitelesítő szolgáltató *pshtest* az erőforráscsoport *PSH – teszt – RG*.</span><span class="sxs-lookup"><span data-stu-id="05228-112">Get Attestation Provider *pshtest* in Resource Group *psh-test-rg*.</span></span>

### <span data-ttu-id="05228-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="05228-113">Example 2</span></span>
```powershell
PS C:\> Get-AzAttestation -DefaultProvider
Id                : /providers/Microsoft.Attestation/attestationProviders/sharedeus2
Location          : East US 2
ResourceGroupName :
Name              : sharedeus2
Status            : Ready
TrustModel        : AAD
AttestUri         : https://sharedeus2.eus2.attest.azure.net
Tags              :
TagsTable         :

Id                : /providers/Microsoft.Attestation/attestationProviders/sharedcus
Location          : Central US
ResourceGroupName :
Name              : sharedcus
Status            : Ready
TrustModel        : AAD
AttestUri         : https://sharedcus.cus.attest.azure.net
Tags              :
TagsTable         :

Id                : /providers/Microsoft.Attestation/attestationProviders/shareduks
Location          : UK South
ResourceGroupName :
Name              : shareduks
Status            : Ready
TrustModel        : AAD
AttestUri         : https://shareduks.uks.attest.azure.net
Tags              :
TagsTable         :
```

<span data-ttu-id="05228-114">Az összes rendelkezésre álló tanúsítvány alapértelmezett szolgáltatójának beszerzése</span><span class="sxs-lookup"><span data-stu-id="05228-114">Get all available Attestation Default Providers</span></span>

### <span data-ttu-id="05228-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="05228-115">Example 3</span></span>
```powershell
PS C:\> Get-AzAttestation -DefaultProvider -Location "East US 2"
Id                : /providers/Microsoft.Attestation/attestationProviders/sharedeus2
Location          : East US 2
ResourceGroupName :
Name              : sharedeus2
Status            : Ready
TrustModel        : AAD
AttestUri         : https://sharedeus2.eus2.attest.azure.net
Tags              :
TagsTable         :
```

<span data-ttu-id="05228-116">Tanúsítvány kérése az alapértelmezett szolgáltatótól a *Kelet-Amerikai Egyesült államokbeli* helyről</span><span class="sxs-lookup"><span data-stu-id="05228-116">Get Attestation Default Provider from Location *East US 2*</span></span>

## <span data-ttu-id="05228-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="05228-117">PARAMETERS</span></span>

### <span data-ttu-id="05228-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05228-118">-DefaultProfile</span></span>
<span data-ttu-id="05228-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="05228-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="05228-120">-DefaultProvider</span><span class="sxs-lookup"><span data-stu-id="05228-120">-DefaultProvider</span></span>
<span data-ttu-id="05228-121">Ez a beállítás az alapértelmezett tanúsítvány-szolgáltató kérése.</span><span class="sxs-lookup"><span data-stu-id="05228-121">Specifies this is the request to a default attestation provider.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultProviderParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05228-122">-Hely</span><span class="sxs-lookup"><span data-stu-id="05228-122">-Location</span></span>
<span data-ttu-id="05228-123">Az alapértelmezett tanúsítvány-szolgáltató helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="05228-123">Specifies the Location of the default attestation provider.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultProviderParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05228-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="05228-124">-Name</span></span>
<span data-ttu-id="05228-125">Tanúsítvány neve.</span><span class="sxs-lookup"><span data-stu-id="05228-125">Attestation Name.</span></span>

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

### <span data-ttu-id="05228-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05228-126">-ResourceGroupName</span></span>
<span data-ttu-id="05228-127">A lekérdezett tanúsítványhoz tartozó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="05228-127">Specifies the name of the resource group associated with the attestation being queried.</span></span>

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

### <span data-ttu-id="05228-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="05228-128">-ResourceId</span></span>
<span data-ttu-id="05228-129">A lekérdezett tanúsítvánnyal társított ResourceID nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="05228-129">Specifies the name of the ResourceID associated with the attestation being queried</span></span>

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

### <span data-ttu-id="05228-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05228-130">CommonParameters</span></span>
<span data-ttu-id="05228-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="05228-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05228-132">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="05228-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05228-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="05228-133">INPUTS</span></span>

### <span data-ttu-id="05228-134">System. String</span><span class="sxs-lookup"><span data-stu-id="05228-134">System.String</span></span>

## <span data-ttu-id="05228-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="05228-135">OUTPUTS</span></span>

### <span data-ttu-id="05228-136">Microsoft. Azure. commands. igazolás. models. PSAttestation</span><span class="sxs-lookup"><span data-stu-id="05228-136">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span></span>

## <span data-ttu-id="05228-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="05228-137">NOTES</span></span>

## <span data-ttu-id="05228-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="05228-138">RELATED LINKS</span></span>
