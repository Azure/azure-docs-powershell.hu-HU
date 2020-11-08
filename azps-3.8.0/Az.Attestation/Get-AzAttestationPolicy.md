---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/get-azattestationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Get-AzAttestationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Get-AzAttestationPolicy.md
ms.openlocfilehash: 0c36f5fb87e3d247a48031bdc735c077a577ac27
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012735"
---
# <span data-ttu-id="bcf25-101">Get-AzAttestationPolicy</span><span class="sxs-lookup"><span data-stu-id="bcf25-101">Get-AzAttestationPolicy</span></span>

## <span data-ttu-id="bcf25-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bcf25-102">SYNOPSIS</span></span>
<span data-ttu-id="bcf25-103">A házirendet a bérlőtől kapja az Azure tanúsítványban.</span><span class="sxs-lookup"><span data-stu-id="bcf25-103">Gets the policy from a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="bcf25-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bcf25-104">SYNTAX</span></span>

### <span data-ttu-id="bcf25-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="bcf25-105">NameParameterSet</span></span>
```
Get-AzAttestationPolicy [-Name] <String> [-ResourceGroupName] <String> -Tee <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bcf25-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bcf25-106">ResourceIdParameterSet</span></span>
```
Get-AzAttestationPolicy [-ResourceId] <String> -Tee <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bcf25-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="bcf25-107">DESCRIPTION</span></span>
<span data-ttu-id="bcf25-108">Az Get-AzAttestationPolicy parancsmag az Azure-tanúsítványban lévő bérlői fiókban kapja meg a házirendet.</span><span class="sxs-lookup"><span data-stu-id="bcf25-108">The Get-AzAttestationPolicy cmdlet gets the policy from a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="bcf25-109">Példák</span><span class="sxs-lookup"><span data-stu-id="bcf25-109">EXAMPLES</span></span>

### <span data-ttu-id="bcf25-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="bcf25-110">Example 1</span></span>
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

<span data-ttu-id="bcf25-111">Megkapja a házirendet a tanúsítvány-szolgáltató *pshtest* a Tee Type *SgxEnclave*.</span><span class="sxs-lookup"><span data-stu-id="bcf25-111">Gets the policy for Attestation Provider *pshtest* for Tee type *SgxEnclave*.</span></span>

## <span data-ttu-id="bcf25-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bcf25-112">PARAMETERS</span></span>

### <span data-ttu-id="bcf25-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcf25-113">-DefaultProfile</span></span>
<span data-ttu-id="bcf25-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bcf25-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bcf25-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="bcf25-115">-Name</span></span>
<span data-ttu-id="bcf25-116">A bérlő nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bcf25-116">Specifies a name of the tenant.</span></span>
<span data-ttu-id="bcf25-117">Ez a parancsmag a megadott bérlői tanúsítványra vonatkozó házirendet kapja meg.</span><span class="sxs-lookup"><span data-stu-id="bcf25-117">This cmdlet gets the attestation policy for the tenant that this parameter specifies.</span></span>

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

### <span data-ttu-id="bcf25-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bcf25-118">-ResourceGroupName</span></span>
<span data-ttu-id="bcf25-119">A tanúsítvány-szolgáltató erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bcf25-119">Specifies the resource group name of an attestation provider.</span></span>

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

### <span data-ttu-id="bcf25-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bcf25-120">-ResourceId</span></span>
<span data-ttu-id="bcf25-121">A hitelesítő szolgáltató ResourceID adja meg.</span><span class="sxs-lookup"><span data-stu-id="bcf25-121">Specifies the ResourceID of an attestation provider.</span></span>

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

### <span data-ttu-id="bcf25-122">-Tee</span><span class="sxs-lookup"><span data-stu-id="bcf25-122">-Tee</span></span>
<span data-ttu-id="bcf25-123">A megbízható végrehajtási környezet típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="bcf25-123">Specifies a type of Trusted Execution Environment.</span></span>
<span data-ttu-id="bcf25-124">Négy típusú környezetet támogatunk: SgxEnclave, OpenEnclave, CyResComponent és VBSEnclave.</span><span class="sxs-lookup"><span data-stu-id="bcf25-124">We support four types of environment: SgxEnclave, OpenEnclave, CyResComponent and VBSEnclave.</span></span>

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

### <span data-ttu-id="bcf25-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="bcf25-125">-Confirm</span></span>
<span data-ttu-id="bcf25-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="bcf25-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bcf25-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bcf25-127">-WhatIf</span></span>
<span data-ttu-id="bcf25-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="bcf25-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bcf25-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bcf25-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bcf25-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcf25-130">CommonParameters</span></span>
<span data-ttu-id="bcf25-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bcf25-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcf25-132">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="bcf25-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcf25-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bcf25-133">INPUTS</span></span>

### <span data-ttu-id="bcf25-134">System. String</span><span class="sxs-lookup"><span data-stu-id="bcf25-134">System.String</span></span>

## <span data-ttu-id="bcf25-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bcf25-135">OUTPUTS</span></span>

### <span data-ttu-id="bcf25-136">Microsoft. Azure. commands. igazolás. models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="bcf25-136">Microsoft.Azure.Commands.Attestation.Models.PSPolicy</span></span>

## <span data-ttu-id="bcf25-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bcf25-137">NOTES</span></span>

## <span data-ttu-id="bcf25-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bcf25-138">RELATED LINKS</span></span>
