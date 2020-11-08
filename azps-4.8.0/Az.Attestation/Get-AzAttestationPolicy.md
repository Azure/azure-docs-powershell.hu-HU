---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/get-azattestationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Get-AzAttestationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Get-AzAttestationPolicy.md
ms.openlocfilehash: 64a74902d1a5b10ed36c635b58910246634e68b0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024234"
---
# <span data-ttu-id="4175d-101">Get-AzAttestationPolicy</span><span class="sxs-lookup"><span data-stu-id="4175d-101">Get-AzAttestationPolicy</span></span>

## <span data-ttu-id="4175d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4175d-102">SYNOPSIS</span></span>
<span data-ttu-id="4175d-103">A házirendet a bérlőtől kapja az Azure tanúsítványban.</span><span class="sxs-lookup"><span data-stu-id="4175d-103">Gets the policy from a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="4175d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4175d-104">SYNTAX</span></span>

### <span data-ttu-id="4175d-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="4175d-105">NameParameterSet</span></span>
```
Get-AzAttestationPolicy [-Name] <String> [-ResourceGroupName] <String> -Tee <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4175d-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4175d-106">ResourceIdParameterSet</span></span>
```
Get-AzAttestationPolicy [-ResourceId] <String> -Tee <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4175d-107">DefaultProviderParameterSet</span><span class="sxs-lookup"><span data-stu-id="4175d-107">DefaultProviderParameterSet</span></span>
```
Get-AzAttestationPolicy [-Location] <String> [-DefaultProvider] -Tee <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4175d-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="4175d-108">DESCRIPTION</span></span>
<span data-ttu-id="4175d-109">Az Get-AzAttestationPolicy parancsmag az Azure-tanúsítványban lévő bérlői fiókban kapja meg a házirendet.</span><span class="sxs-lookup"><span data-stu-id="4175d-109">The Get-AzAttestationPolicy cmdlet gets the policy from a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="4175d-110">Példák</span><span class="sxs-lookup"><span data-stu-id="4175d-110">EXAMPLES</span></span>

### <span data-ttu-id="4175d-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="4175d-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAttestationPolicy -Name pshtest -ResourceGroupName psh-test-rg -Tee SgxEnclave                                                                                                                                                                                                                    
Text       : version= 1.0;
             authorizationrules{
                 c:[type=="$is-debuggable"] => permit();
             };
             issuancerules{
                 c:[type=="$is-debuggable"] => issue(type="is-debuggable", value=c.value);
                 c:[type=="$sgx-mrsigner"] => issue(type="sgx-mrsigner", value=c.value);
                 c:[type=="$sgx-mrenclave"] => issue(type="sgx-mrenclave", value=c.value);
                 c:[type=="$product-id"] => issue(type="product-id", value=c.value);
                 c:[type=="$svn"] => issue(type="svn", value=c.value);
                 c:[type=="$tee"] => issue(type="tee", value=c.value);
                 c:[type=="$tee-future"] => issue(type="tee-future", value=c.value);
             };

TextLength : 604
Jwt        : eyJhbGciOiJub25lIn0.eyJBdHRlc3RhdGlvblBvbGljeSI6ICJkbVZ5YzJsdmJqMGdNUzR3T3cwS1lYVjBhRzl5YVhwaGRHbHZibkoxYkdWemV3MEtJQ0FnSUdNNlczUjVjR1U5UFNJa2FYTXRaR1ZpZFdkbllXSnNaU0pkSUQwLUlIQmxjbTFwZENncE93MEtmVHNOQ21semMzVmhibU5sY25Wc1pYTjdEUW9nSUNBZ1l6cGJkSGx3WlQwOUlpUnBjeTFrWldKMVoyZGhZbXhsSWwwZ1BUNGdhWE56ZFdVb2RIbHdaVDBpYVhNdFpHVmlkV2RuWVdKc1pTSXNJSFpoYkhWbFBXTXVkbUZzZFdVcE93MEtJQ0FnSUdNNlczUjVjR1U5UFNJa2MyZDRMVzF5YzJsbmJtVnlJbDBnUFQ0Z2FYTnpkV1VvZEhsd1pUMGljMmQ0TFcxeWMybG5ibVZ5SWl3Z2RtRnNkV1U5WXk1MllXeDFaU2s3RFFvZ0lDQWdZenBiZEhsd1pUMDlJaVJ6WjNndGJYSmxibU5zWVhabElsMGdQVDRnYVhOemRXVW9kSGx3WlQwaWMyZDRMVzF5Wlc1amJHRjJaU0lzSUhaaGJIVmxQV011ZG1Gc2RXVXBPdzBLSUNBZ0lHTTZXM1I1Y0dVOVBTSWtjSEp2WkhWamRDMXBaQ0pkSUQwLUlHbHpjM1ZsS0hSNWNHVTlJbkJ5YjJSMVkzUXRhV1FpTENCMllXeDFaVDFqTG5aaGJIVmxLVHNOQ2lBZ0lDQmpPbHQwZVhCbFBUMGlKSE4yYmlKZElEMC1JR2x6YzNWbEtIUjVjR1U5SW5OMmJpSXNJSFpoYkhWbFBXTXVkbUZzZFdVcE93MEtJQ0FnSUdNNlczUjVjR1U5UFNJa2RHVmxJbDBnUFQ0Z2FYTnpkV1VvZEhsd1pUMGlkR1ZsSWl3Z2RtRnNkV1U5WXk1MllXeDFaU2s3RFFvZ0lDQWdZenBiZEhsd1pUMDlJaVIwWldVdFpuVjBkWEpsSWwwZ1BUNGdhWE56ZFdVb2RIbHdaVDBpZEdWbExXWjFkSFZ5WlNJc0lIWmhiSFZsUFdNdWRtRnNkV1VwT3cwS2ZUc05DZyJ9.
JwtLength  : 1129
Algorithm  : none
```

<span data-ttu-id="4175d-112">Megkapja a házirendet a tanúsítvány-szolgáltató *pshtest* a Tee Type *SgxEnclave*.</span><span class="sxs-lookup"><span data-stu-id="4175d-112">Gets the policy for Attestation Provider *pshtest* for Tee type *SgxEnclave*.</span></span>

### <span data-ttu-id="4175d-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="4175d-113">Example 2</span></span>
```powershell
PS C:\> Get-AzAttestationPolicy -DefaultProvider -Location "UK South" -Tee SgxEnclave
Text       : version= 1.0;authorizationrules{c:[type=="$is-debuggable"] => permit();};issuancerules{c:[type=="$is-debuggable"] => issue(type="is-debuggable",
             value=c.value);c:[type=="$sgx-mrsigner"] => issue(type="sgx-mrsigner", value=c.value);c:[type=="$sgx-mrenclave"] => issue(type="sgx-mrenclave",
             value=c.value);c:[type=="$product-id"] => issue(type="product-id", value=c.value);c:[type=="$svn"] => issue(type="svn", value=c.value);c:[type=="$tee"]
             => issue(type="tee", value=c.value);};
TextLength : 479
Jwt        : eyJhbGciOiJub25lIn0.eyJBdHRlc3RhdGlvblBvbGljeSI6ICJkbVZ5YzJsdmJqMGdNUzR3TzJGMWRHaHZjbWw2WVhScGIyNXlkV3hsYzN0ak9sdDBlWEJsUFQwaUpHbHpMV1JsWW5WbloyRmliR1Vp
             WFNBOVBpQndaWEp0YVhRb0tUdDlPMmx6YzNWaGJtTmxjblZzWlhON1l6cGJkSGx3WlQwOUlpUnBjeTFrWldKMVoyZGhZbXhsSWwwZ1BUNGdhWE56ZFdVb2RIbHdaVDBpYVhNdFpHVmlkV2RuWVdKc1pT
             SXNJSFpoYkhWbFBXTXVkbUZzZFdVcE8yTTZXM1I1Y0dVOVBTSWtjMmQ0TFcxeWMybG5ibVZ5SWwwZ1BUNGdhWE56ZFdVb2RIbHdaVDBpYzJkNExXMXljMmxuYm1WeUlpd2dkbUZzZFdVOVl5NTJZV3gx
             WlNrN1l6cGJkSGx3WlQwOUlpUnpaM2d0YlhKbGJtTnNZWFpsSWwwZ1BUNGdhWE56ZFdVb2RIbHdaVDBpYzJkNExXMXlaVzVqYkdGMlpTSXNJSFpoYkhWbFBXTXVkbUZzZFdVcE8yTTZXM1I1Y0dVOVBT
             SWtjSEp2WkhWamRDMXBaQ0pkSUQwLUlHbHpjM1ZsS0hSNWNHVTlJbkJ5YjJSMVkzUXRhV1FpTENCMllXeDFaVDFqTG5aaGJIVmxLVHRqT2x0MGVYQmxQVDBpSkhOMmJpSmRJRDAtSUdsemMzVmxLSFI1
             Y0dVOUluTjJiaUlzSUhaaGJIVmxQV011ZG1Gc2RXVXBPMk02VzNSNWNHVTlQU0lrZEdWbElsMGdQVDRnYVhOemRXVW9kSGx3WlQwaWRHVmxJaXdnZG1Gc2RXVTlZeTUyWVd4MVpTazdmVHMifQ.
JwtLength  : 907
Algorithm  : none
```

<span data-ttu-id="4175d-114">Beolvassa a házirendet a tanúsítványok alapértelmezett szolgáltatójának: a *Dél-angol* (Tee) típusú *SgxEnclave*.</span><span class="sxs-lookup"><span data-stu-id="4175d-114">Gets the policy for Attestation Default Provider from Location *UK South* for Tee type *SgxEnclave*.</span></span>

## <span data-ttu-id="4175d-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4175d-115">PARAMETERS</span></span>

### <span data-ttu-id="4175d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4175d-116">-DefaultProfile</span></span>
<span data-ttu-id="4175d-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4175d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4175d-118">-DefaultProvider</span><span class="sxs-lookup"><span data-stu-id="4175d-118">-DefaultProvider</span></span>
<span data-ttu-id="4175d-119">Ez a beállítás az alapértelmezett tanúsítvány-szolgáltató kérése.</span><span class="sxs-lookup"><span data-stu-id="4175d-119">Specifies this is the request to a default attestation provider.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultProviderParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4175d-120">-Hely</span><span class="sxs-lookup"><span data-stu-id="4175d-120">-Location</span></span>
<span data-ttu-id="4175d-121">Az alapértelmezett tanúsítvány-szolgáltató helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4175d-121">Specifies the Location of the default attestation provider.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultProviderParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4175d-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4175d-122">-Name</span></span>
<span data-ttu-id="4175d-123">A bérlő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4175d-123">Specifies a name of the tenant.</span></span>
<span data-ttu-id="4175d-124">Ez a parancsmag a megadott bérlői tanúsítványra vonatkozó házirendet kapja meg.</span><span class="sxs-lookup"><span data-stu-id="4175d-124">This cmdlet gets the attestation policy for the tenant that this parameter specifies.</span></span>

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

### <span data-ttu-id="4175d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4175d-125">-ResourceGroupName</span></span>
<span data-ttu-id="4175d-126">A tanúsítvány-szolgáltató erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4175d-126">Specifies the resource group name of an attestation provider.</span></span>

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

### <span data-ttu-id="4175d-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4175d-127">-ResourceId</span></span>
<span data-ttu-id="4175d-128">A hitelesítő szolgáltató ResourceID adja meg.</span><span class="sxs-lookup"><span data-stu-id="4175d-128">Specifies the ResourceID of an attestation provider.</span></span>

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

### <span data-ttu-id="4175d-129">-Tee</span><span class="sxs-lookup"><span data-stu-id="4175d-129">-Tee</span></span>
<span data-ttu-id="4175d-130">A megbízható végrehajtási környezet típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="4175d-130">Specifies a type of Trusted Execution Environment.</span></span>
<span data-ttu-id="4175d-131">Négy típusú környezetet támogatunk: SgxEnclave, OpenEnclave, CyResComponent és VBSEnclave.</span><span class="sxs-lookup"><span data-stu-id="4175d-131">We support four types of environment: SgxEnclave, OpenEnclave, CyResComponent and VBSEnclave.</span></span>

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

### <span data-ttu-id="4175d-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4175d-132">-Confirm</span></span>
<span data-ttu-id="4175d-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4175d-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4175d-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4175d-134">-WhatIf</span></span>
<span data-ttu-id="4175d-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4175d-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4175d-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4175d-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4175d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4175d-137">CommonParameters</span></span>
<span data-ttu-id="4175d-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4175d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4175d-139">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="4175d-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4175d-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4175d-140">INPUTS</span></span>

### <span data-ttu-id="4175d-141">System. String</span><span class="sxs-lookup"><span data-stu-id="4175d-141">System.String</span></span>

## <span data-ttu-id="4175d-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4175d-142">OUTPUTS</span></span>

### <span data-ttu-id="4175d-143">Microsoft. Azure. commands. igazolás. models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="4175d-143">Microsoft.Azure.Commands.Attestation.Models.PSPolicy</span></span>

## <span data-ttu-id="4175d-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4175d-144">NOTES</span></span>

## <span data-ttu-id="4175d-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4175d-145">RELATED LINKS</span></span>
