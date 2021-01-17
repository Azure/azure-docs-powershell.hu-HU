---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: A9C98F8F-90F2-4BF4-A234-31966FBB975B
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchCertificate.md
ms.openlocfilehash: 26bd35f59ae5e640093c1695e7caf991e1e1e956
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98478377"
---
# <span data-ttu-id="2d9e2-101">Get-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="2d9e2-101">Get-AzBatchCertificate</span></span>

## <span data-ttu-id="2d9e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2d9e2-102">SYNOPSIS</span></span>
<span data-ttu-id="2d9e2-103">Egy Batch-fiók tanúsítványait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="2d9e2-103">Gets the certificates in a Batch account.</span></span>

## <span data-ttu-id="2d9e2-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2d9e2-104">SYNTAX</span></span>

### <span data-ttu-id="2d9e2-105">ODataFilter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2d9e2-105">ODataFilter (Default)</span></span>
```
Get-AzBatchCertificate [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2d9e2-106">Thumbprint</span><span class="sxs-lookup"><span data-stu-id="2d9e2-106">Thumbprint</span></span>
```
Get-AzBatchCertificate [-ThumbprintAlgorithm] <String> [-Thumbprint] <String> [-Select <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2d9e2-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2d9e2-107">DESCRIPTION</span></span>
<span data-ttu-id="2d9e2-108">A **Get-AzBatchCertificate** parancsmag a *BatchContext* paraméter által megadott Azure Batch-fiók tanúsítványait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="2d9e2-108">The **Get-AzBatchCertificate** cmdlet gets the certificates in the Azure Batch account that the *BatchContext* parameter specifies.</span></span>
<span data-ttu-id="2d9e2-109">Egy adott tanúsítvány beszerzéséhez adja meg a *ThumbprintAlgorithm és* *a Thumbprint paramétert.*</span><span class="sxs-lookup"><span data-stu-id="2d9e2-109">To obtain a particular certificate, specify the *ThumbprintAlgorithm* and *Thumbprint* parameters.</span></span>
<span data-ttu-id="2d9e2-110">Adja meg *a Szűrő* paramétert az OData-szűrőnek megfelelő tanúsítványok be szereznie.</span><span class="sxs-lookup"><span data-stu-id="2d9e2-110">Specify the *Filter* parameter to get the certificates that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="2d9e2-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2d9e2-111">EXAMPLES</span></span>

### <span data-ttu-id="2d9e2-112">1. példa: Tanúsítvány lekérve thumbprint-sal</span><span class="sxs-lookup"><span data-stu-id="2d9e2-112">Example 1: Get a certificate by thumbprint</span></span>
```
PS C:\>Get-AzBatchCertificate -ThumbprintAlgorithm "sha1" - Thumbprint "C1E494A415149C5F211C4778B52F2E834A07247C" -BatchContext $Context
Thumbprint                  : c1e494a415149c5f211c4778b52f2e834a07247c
ThumbprintAlgorithm         : sha1
Url                         : https://pstests.eastus.batch.azure.com/certificates(thumbprintAlgorithm=sha1,thumbprint=C1E494A415149C5F211C4778B52F2E834A07247
C)
State                       : Active
StateTransitionTime         : 10/6/2015 6:21:16 PM
PreviousState               :
PreviousStateTransitionTime :
Data                        :
CertificateFormat           :
Password                    :
PublicData                  : MIIB9DCCAWGgAwIBAgIQpUXhwCuAPJRDhl7kY/0PdTAJBgUrDgMCHQUAMBYxFDASBgNVBAMTC0JhdGNoVGVzdDAxMB4XDTE1MTAwMjE2MjkwNVoXDTM5MTIzMTIzNTk
1OVowFjEUMBIGA1UEAxMLQmF0Y2hUZXN0MDEwgZ8wDQYJKoZIhvcNAQEBBQADgY0AMIGJAoGBAM06unpRipn3BmHBM75d0s8w/Wwifci16PoJo4c2V68GwsCCFsNOn5
ypo7BBXo1fpBjrnso5w+koaE5LjxkBSVm+TkogwbKlW6WURTM0O5viRVbPnEEU/Y01Pj5cJElFuLEk9Uoe/r/lP8b5A607t1cPjSXkwhEZEYc3LkHDSo0ZAgMBAAGjS
zBJMEcGA1UdAQRAMD6AEFRsTAsrvF+FmPuICooZXaKhGDAWMRQwEgYDVQQDEwtCYXRjaFRlc3QwMYIQpUXhwCuAPJRDhl7kY/0PdTAJBgUrDgMCHQUAA4GBALt0F8Ep
+8XVE/M2aNtxzlku72gxiOiAo1HmpUaixXx3gl8kdP3xgoKMaq4JskqdLmbJJUnCQ3wmzsdPwjswsW2ycT12zuBddaiS+id98k8U/KYc6FxMgS+H70FYOxARLn7P4FS
SBf/QCyign+BherzezdZ5NBdfzbmWxIMP5iFJ
DeleteCertificateError      :
```

<span data-ttu-id="2d9e2-113">Ez a parancs egyetlen tanúsítványt kap, amely rendelkezik a megadott thumbprint-sal.</span><span class="sxs-lookup"><span data-stu-id="2d9e2-113">This command gets a single certificate that has the specified thumbprint.</span></span>
<span data-ttu-id="2d9e2-114">A tanúsítvány thumbprint algoritmusa sha1.</span><span class="sxs-lookup"><span data-stu-id="2d9e2-114">The certificate thumbprint algorithm is sha1.</span></span>

### <span data-ttu-id="2d9e2-115">2. példa: Szűrt tanúsítványok lekérte</span><span class="sxs-lookup"><span data-stu-id="2d9e2-115">Example 2: Get filtered certificates</span></span>
```
PS C:\>Get-AzBatchCertificate -Filter "state eq 'active'" -BatchContext $Context
Thumbprint                  : 025b351b087a084c5067f5e71eff8591970323f9
ThumbprintAlgorithm         : sha1
Url                         : https://pstests.eastus.batch.azure.com/certificates(thumbprintAlgorithm=sha1,thumbprint=025b351b087a084c5067f5e71eff8591970323f9)
State                       : Active
StateTransitionTime         : 10/6/2015 6:21:17 PM
PreviousState               :
PreviousStateTransitionTime :
Data                        :
CertificateFormat           :
Password                    :
PublicData                  : MIIB9DCCAWGgAwIBAgIQy9W5y8iwhppGhtAG06dHKTAJBgUrDgMCHQUAMBYxFDASBgNVBAMTC0JhdGNoVGVzdDAyMB4XDTE1MTAwMjE2MjkxNFoXDTM5MTIzMTIzNTk
1OVowFjEUMBIGA1UEAxMLQmF0Y2hUZXN0MDIwgZ8wDQYJKoZIhvcNAQEBBQADgY0AMIGJAoGBAJxagvVrlnKfv6hfzSiFJUkdGkPjC3tFiKebK6IaeHzesFdFfupXUE
wT0xOWh9xwa3OVkPECEc/u1sw3iVX/J4AODiwzmOWutoVRpWjxGFpgw9+dPvXMjs/Ue7JL7ag3siHs5EcarW91qKbgtko6i/r4emaRyk60U93TrbWQAWJ9AgMBAAGjS
zBJMEcGA1UdAQRAMD6AEAdqsOpyeXF/uDe7ZGKeez+hGDAWMRQwEgYDVQQDEwtCYXRjaFRlc3QwMoIQy9W5y8iwhppGhtAG06dHKTAJBgUrDgMCHQUAA4GBAC0MaAem
6ByyURFvGnFZyjEepjXC5wcaGq+gguDFe8rG88ceig1ZqewdcmC1y4p05uBhbmETbYVWzJarNsHYq2LTihi4t2J4jt2YVYz/IRdUB82iaFFbJRSPrN+6xD3KM2lve5N
4OjtlZAdiXiSUYFf3I6ypberUsAdba3QQajCN
DeleteCertificateError      :

Thumbprint                  : c1e494a415149c5f211c4778b52f2e834a07247c
ThumbprintAlgorithm         : sha1
Url                         : https://pstests.eastus.batch.azure.com/certificates(thumbprintAlgorithm=sha1,thumbprint=c1e494a415149c5f211c4778b52f2e834a07247c)
State                       : Active
StateTransitionTime         : 10/6/2015 6:21:16 PM
PreviousState               :
PreviousStateTransitionTime :
Data                        :
CertificateFormat           :
Password                    :
PublicData                  : MIIB9DCCAWGgAwIBAgIQpUXhwCuAPJRDhl7kY/0PdTAJBgUrDgMCHQUAMBYxFDASBgNVBAMTC0JhdGNoVGVzdDAxMB4XDTE1MTAwMjE2MjkwNVoXDTM5MTIzMTIzNTk
1OVowFjEUMBIGA1UEAxMLQmF0Y2hUZXN0MDEwgZ8wDQYJKoZIhvcNAQEBBQADgY0AMIGJAoGBAM06unpRipn3BmHBM75d0s8w/Wwifci16PoJo4c2V68GwsCCFsNOn5
ypo7BBXo1fpBjrnso5w+koaE5LjxkBSVm+TkogwbKlW6WURTM0O5viRVbPnEEU/Y01Pj5cJElFuLEk9Uoe/r/lP8b5A607t1cPjSXkwhEZEYc3LkHDSo0ZAgMBAAGjS
zBJMEcGA1UdAQRAMD6AEFRsTAsrvF+FmPuICooZXaKhGDAWMRQwEgYDVQQDEwtCYXRjaFRlc3QwMYIQpUXhwCuAPJRDhl7kY/0PdTAJBgUrDgMCHQUAA4GBALt0F8Ep
+8XVE/M2aNtxzlku72gxiOiAo1HmpUaixXx3gl8kdP3xgoKMaq4JskqdLmbJJUnCQ3wmzsdPwjswsW2ycT12zuBddaiS+id98k8U/KYc6FxMgS+H70FYOxARLn7P4FS
SBf/QCyign+BherzezdZ5NBdfzbmWxIMP5iFJ
DeleteCertificateError      :
```

<span data-ttu-id="2d9e2-116">Ez a parancs az aktív állapotban lévő összes tanúsítványt a Batch-fiókból kapja meg.</span><span class="sxs-lookup"><span data-stu-id="2d9e2-116">This command gets all certificates in the active state from the Batch account.</span></span>
<span data-ttu-id="2d9e2-117">A *Szűrő* paraméter az államot határozza meg.</span><span class="sxs-lookup"><span data-stu-id="2d9e2-117">The *Filter* parameter specifies the state.</span></span>

## <span data-ttu-id="2d9e2-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2d9e2-118">PARAMETERS</span></span>

### <span data-ttu-id="2d9e2-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="2d9e2-119">-BatchContext</span></span>
<span data-ttu-id="2d9e2-120">Azt a **BatchAccountContext példányt** adja meg, amely a parancsmagot használja a Batch szolgáltatáshoz való interakcióhoz.</span><span class="sxs-lookup"><span data-stu-id="2d9e2-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="2d9e2-121">Ha a Get-AzBatchAccount parancsmaggal szerezze be a BatchAccountContext parancsmagot, akkor a Batch szolgáltatás használata során az Azure Active Directory-hitelesítést fogja használni a rendszer.</span><span class="sxs-lookup"><span data-stu-id="2d9e2-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="2d9e2-122">Ha ehelyett megosztott kulcsú hitelesítést használ, a Get-AzBatchAccountKey parancsmaggal töltse ki a BatchAccountContext objektumot a hozzáférési kulcsokkal.</span><span class="sxs-lookup"><span data-stu-id="2d9e2-122">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="2d9e2-123">Megosztott kulcs hitelesítése esetén a rendszer alapértelmezés szerint az elsődleges hozzáférési kulcsot használja.</span><span class="sxs-lookup"><span data-stu-id="2d9e2-123">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="2d9e2-124">A használni használt kulcs módosítása a BatchAccountContext.KeyInUse tulajdonsággal.</span><span class="sxs-lookup"><span data-stu-id="2d9e2-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2d9e2-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d9e2-125">-DefaultProfile</span></span>
<span data-ttu-id="2d9e2-126">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2d9e2-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2d9e2-127">-Filter</span><span class="sxs-lookup"><span data-stu-id="2d9e2-127">-Filter</span></span>
<span data-ttu-id="2d9e2-128">OData-szűrő záradékot ad meg.</span><span class="sxs-lookup"><span data-stu-id="2d9e2-128">Specifies an OData filter clause.</span></span>
<span data-ttu-id="2d9e2-129">Ha ezt a paramétert adja meg, ez a parancsmag a szűrőnek megfelelő tanúsítványokat kapja.</span><span class="sxs-lookup"><span data-stu-id="2d9e2-129">If you specify this parameter, this cmdlet gets the certificates that match the filter.</span></span>

```yaml
Type: System.String
Parameter Sets: ODataFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d9e2-130">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="2d9e2-130">-MaxCount</span></span>
<span data-ttu-id="2d9e2-131">Azt adja meg, hogy legfeljebb hány tanúsítványt kell visszaadni.</span><span class="sxs-lookup"><span data-stu-id="2d9e2-131">Specifies the maximum number of certificates to return.</span></span>
<span data-ttu-id="2d9e2-132">Ha nullát (0) vagy kisebb értéket ad meg, a parancsmag nem használ felső korlátot.</span><span class="sxs-lookup"><span data-stu-id="2d9e2-132">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="2d9e2-133">Az alapértelmezett érték 1000.</span><span class="sxs-lookup"><span data-stu-id="2d9e2-133">The default value is 1000.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ODataFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d9e2-134">-Válassza a</span><span class="sxs-lookup"><span data-stu-id="2d9e2-134">-Select</span></span>
<span data-ttu-id="2d9e2-135">OData-választó záradékot ad meg.</span><span class="sxs-lookup"><span data-stu-id="2d9e2-135">Specifies an OData select clause.</span></span>
<span data-ttu-id="2d9e2-136">A paraméter értékét megadva az összes objektumtulajdonság helyett konkrét tulajdonságokat kap.</span><span class="sxs-lookup"><span data-stu-id="2d9e2-136">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d9e2-137">-Thumbprint</span><span class="sxs-lookup"><span data-stu-id="2d9e2-137">-Thumbprint</span></span>
<span data-ttu-id="2d9e2-138">A parancsmag által lekért tanúsítvány thumbprintja.</span><span class="sxs-lookup"><span data-stu-id="2d9e2-138">Specifies the thumbprint of the certificate that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: Thumbprint
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d9e2-139">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="2d9e2-139">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="2d9e2-140">A Thumbprint paraméter származtatására *használt algoritmus.*</span><span class="sxs-lookup"><span data-stu-id="2d9e2-140">Specifies the algorithm used to derive the *Thumbprint* parameter.</span></span>
<span data-ttu-id="2d9e2-141">Jelenleg az egyetlen érvényes érték az sha1.</span><span class="sxs-lookup"><span data-stu-id="2d9e2-141">Currently, the only valid value is sha1.</span></span>

```yaml
Type: System.String
Parameter Sets: Thumbprint
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d9e2-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d9e2-142">CommonParameters</span></span>
<span data-ttu-id="2d9e2-143">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d9e2-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d9e2-144">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2d9e2-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d9e2-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2d9e2-145">INPUTS</span></span>

### <span data-ttu-id="2d9e2-146">System.String</span><span class="sxs-lookup"><span data-stu-id="2d9e2-146">System.String</span></span>

### <span data-ttu-id="2d9e2-147">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="2d9e2-147">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="2d9e2-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2d9e2-148">OUTPUTS</span></span>

### <span data-ttu-id="2d9e2-149">Microsoft.Azure.Commands.Bat. Models.PSCertificate</span><span class="sxs-lookup"><span data-stu-id="2d9e2-149">Microsoft.Azure.Commands.Batch.Models.PSCertificate</span></span>

## <span data-ttu-id="2d9e2-150">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2d9e2-150">NOTES</span></span>

## <span data-ttu-id="2d9e2-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2d9e2-151">RELATED LINKS</span></span>

[<span data-ttu-id="2d9e2-152">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="2d9e2-152">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="2d9e2-153">New-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="2d9e2-153">New-AzBatchCertificate</span></span>](./New-AzBatchCertificate.md)

[<span data-ttu-id="2d9e2-154">Remove-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="2d9e2-154">Remove-AzBatchCertificate</span></span>](./Remove-AzBatchCertificate.md)

[<span data-ttu-id="2d9e2-155">Azure Batch-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="2d9e2-155">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
