---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/powershell/module/az.attestation/get-azattestation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Get-AzAttestation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Get-AzAttestation.md
ms.openlocfilehash: 73e51981dc57c4bc81f530f32b597c619b0bab78
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935401"
---
# <span data-ttu-id="a1211-101">Get-AzAttestation</span><span class="sxs-lookup"><span data-stu-id="a1211-101">Get-AzAttestation</span></span>

## <span data-ttu-id="a1211-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1211-102">SYNOPSIS</span></span>
<span data-ttu-id="a1211-103">Igazolást kap.</span><span class="sxs-lookup"><span data-stu-id="a1211-103">Gets an attestation.</span></span>

## <span data-ttu-id="a1211-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a1211-104">SYNTAX</span></span>

### <span data-ttu-id="a1211-105">NameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a1211-105">NameParameterSet (Default)</span></span>
```
Get-AzAttestation [-Name] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a1211-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a1211-106">ResourceIdParameterSet</span></span>
```
Get-AzAttestation [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a1211-107">DefaultProviderParameterSet</span><span class="sxs-lookup"><span data-stu-id="a1211-107">DefaultProviderParameterSet</span></span>
```
Get-AzAttestation [[-Location] <String>] [-DefaultProvider] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a1211-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a1211-108">DESCRIPTION</span></span>
<span data-ttu-id="a1211-109">A Get-AzAttestation parancsmag információkat kap az előfizetésben való atteálásról.</span><span class="sxs-lookup"><span data-stu-id="a1211-109">The Get-AzAttestation cmdlet gets information about the attestation in a subscription.</span></span>

## <span data-ttu-id="a1211-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a1211-110">EXAMPLES</span></span>

### <span data-ttu-id="a1211-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="a1211-111">Example 1</span></span>
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

<span data-ttu-id="a1211-112">Get Attestation Provider *pshtest* in Resource Group *psh-test-rg.*</span><span class="sxs-lookup"><span data-stu-id="a1211-112">Get Attestation Provider *pshtest* in Resource Group *psh-test-rg*.</span></span>

### <span data-ttu-id="a1211-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="a1211-113">Example 2</span></span>
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

<span data-ttu-id="a1211-114">Az összes elérhető attestation alapértelmezett szolgáltató igénybevéve</span><span class="sxs-lookup"><span data-stu-id="a1211-114">Get all available Attestation Default Providers</span></span>

### <span data-ttu-id="a1211-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="a1211-115">Example 3</span></span>
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

<span data-ttu-id="a1211-116">Az Alapértelmezett szolgáltató beállítása az Us *2.* helyről</span><span class="sxs-lookup"><span data-stu-id="a1211-116">Get Attestation Default Provider from Location *East US 2*</span></span>

## <span data-ttu-id="a1211-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a1211-117">PARAMETERS</span></span>

### <span data-ttu-id="a1211-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1211-118">-DefaultProfile</span></span>
<span data-ttu-id="a1211-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a1211-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1211-120">-DefaultProvider</span><span class="sxs-lookup"><span data-stu-id="a1211-120">-DefaultProvider</span></span>
<span data-ttu-id="a1211-121">Azt adja meg, hogy ez egy alapértelmezett szolgáltatóhoz való kérelem.</span><span class="sxs-lookup"><span data-stu-id="a1211-121">Specifies this is the request to a default attestation provider.</span></span>

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

### <span data-ttu-id="a1211-122">-Location</span><span class="sxs-lookup"><span data-stu-id="a1211-122">-Location</span></span>
<span data-ttu-id="a1211-123">Az alapértelmezett szolgáltató helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a1211-123">Specifies the Location of the default attestation provider.</span></span>

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

### <span data-ttu-id="a1211-124">-Name</span><span class="sxs-lookup"><span data-stu-id="a1211-124">-Name</span></span>
<span data-ttu-id="a1211-125">Attestation Name (Igazolás neve) stb.</span><span class="sxs-lookup"><span data-stu-id="a1211-125">Attestation Name.</span></span>

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

### <span data-ttu-id="a1211-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1211-126">-ResourceGroupName</span></span>
<span data-ttu-id="a1211-127">A lekérdezett igazolással társított erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a1211-127">Specifies the name of the resource group associated with the attestation being queried.</span></span>

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

### <span data-ttu-id="a1211-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a1211-128">-ResourceId</span></span>
<span data-ttu-id="a1211-129">A lekérdezett igazoláshoz társított Erőforrásazonosító nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a1211-129">Specifies the name of the ResourceID associated with the attestation being queried</span></span>

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

### <span data-ttu-id="a1211-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1211-130">CommonParameters</span></span>
<span data-ttu-id="a1211-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1211-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1211-132">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a1211-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1211-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a1211-133">INPUTS</span></span>

### <span data-ttu-id="a1211-134">System.String</span><span class="sxs-lookup"><span data-stu-id="a1211-134">System.String</span></span>

## <span data-ttu-id="a1211-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a1211-135">OUTPUTS</span></span>

### <span data-ttu-id="a1211-136">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span><span class="sxs-lookup"><span data-stu-id="a1211-136">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span></span>

## <span data-ttu-id="a1211-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a1211-137">NOTES</span></span>

## <span data-ttu-id="a1211-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a1211-138">RELATED LINKS</span></span>
