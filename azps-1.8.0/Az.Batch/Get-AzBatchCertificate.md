---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: A9C98F8F-90F2-4BF4-A234-31966FBB975B
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchCertificate.md
ms.openlocfilehash: ed1b4baac3d22789fe08964e4b4d31b53eee7223
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/13/2020
ms.locfileid: "93671896"
---
# <span data-ttu-id="d4b8f-101">Get-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="d4b8f-101">Get-AzBatchCertificate</span></span>

## <span data-ttu-id="d4b8f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d4b8f-102">SYNOPSIS</span></span>
<span data-ttu-id="d4b8f-103">Egy köteg fiókban kapja meg a tanúsítványokat.</span><span class="sxs-lookup"><span data-stu-id="d4b8f-103">Gets the certificates in a Batch account.</span></span>

## <span data-ttu-id="d4b8f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d4b8f-104">SYNTAX</span></span>

### <span data-ttu-id="d4b8f-105">ODataFilter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d4b8f-105">ODataFilter (Default)</span></span>
```
Get-AzBatchCertificate [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d4b8f-106">Ujjlenyomat</span><span class="sxs-lookup"><span data-stu-id="d4b8f-106">Thumbprint</span></span>
```
Get-AzBatchCertificate [-ThumbprintAlgorithm] <String> [-Thumbprint] <String> [-Select <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d4b8f-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="d4b8f-107">DESCRIPTION</span></span>
<span data-ttu-id="d4b8f-108">A **Get-AzBatchCertificate** parancsmag az Azure-köteg fiókjában kapja meg a tanúsítványokat, amelyeket a *BatchContext* paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="d4b8f-108">The **Get-AzBatchCertificate** cmdlet gets the certificates in the Azure Batch account that the *BatchContext* parameter specifies.</span></span>
<span data-ttu-id="d4b8f-109">Ha egy adott tanúsítványt szeretne beolvasni, adja meg a *ThumbprintAlgorithm* és az *ujjlenyomat* paramétert.</span><span class="sxs-lookup"><span data-stu-id="d4b8f-109">To obtain a particular certificate, specify the *ThumbprintAlgorithm* and *Thumbprint* parameters.</span></span>
<span data-ttu-id="d4b8f-110">Adja meg a *szűrő* paramétert a megnyitott Data Protocol (OData) szűrővel megegyező tanúsítványok beolvasásához.</span><span class="sxs-lookup"><span data-stu-id="d4b8f-110">Specify the *Filter* parameter to get the certificates that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="d4b8f-111">Példák</span><span class="sxs-lookup"><span data-stu-id="d4b8f-111">EXAMPLES</span></span>

### <span data-ttu-id="d4b8f-112">1. példa: tanúsítvány beszerzése ujjlenyomat alapján</span><span class="sxs-lookup"><span data-stu-id="d4b8f-112">Example 1: Get a certificate by thumbprint</span></span>
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

<span data-ttu-id="d4b8f-113">Ez a parancs egyetlen olyan tanúsítványt kap, amely a megadott ujjlenyomatot tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="d4b8f-113">This command gets a single certificate that has the specified thumbprint.</span></span>
<span data-ttu-id="d4b8f-114">A tanúsítvány ujjlenyomat-algoritmusa SHA1.</span><span class="sxs-lookup"><span data-stu-id="d4b8f-114">The certificate thumbprint algorithm is sha1.</span></span>

### <span data-ttu-id="d4b8f-115">2. példa: szűrt tanúsítványok beolvasása</span><span class="sxs-lookup"><span data-stu-id="d4b8f-115">Example 2: Get filtered certificates</span></span>
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

<span data-ttu-id="d4b8f-116">Ez a parancs a köteg fiókból az aktív állapot összes tanúsítványát beolvassa.</span><span class="sxs-lookup"><span data-stu-id="d4b8f-116">This command gets all certificates in the active state from the Batch account.</span></span>
<span data-ttu-id="d4b8f-117">A *szűrő* paraméter az államot adja meg.</span><span class="sxs-lookup"><span data-stu-id="d4b8f-117">The *Filter* parameter specifies the state.</span></span>

## <span data-ttu-id="d4b8f-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d4b8f-118">PARAMETERS</span></span>

### <span data-ttu-id="d4b8f-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="d4b8f-119">-BatchContext</span></span>
<span data-ttu-id="d4b8f-120">Azt a **BatchAccountContext** -példányt adja meg, amelyre a parancsmag a kötegelt szolgáltatással való interakciót használja.</span><span class="sxs-lookup"><span data-stu-id="d4b8f-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="d4b8f-121">Ha a Get-AzBatchAccount parancsmagot használja az BatchAccountContext, akkor az Azure Active Directory-hitelesítést a köteg szolgáltatással való interakció során fogja használni.</span><span class="sxs-lookup"><span data-stu-id="d4b8f-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="d4b8f-122">Ha inkább a megosztott kulcsos hitelesítést szeretné használni, használja az Get-AzBatchAccountKeys parancsmagot egy BatchAccountContext objektum eléréséhez a hozzá tartozó elérési kulcsok kitöltésével.</span><span class="sxs-lookup"><span data-stu-id="d4b8f-122">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="d4b8f-123">A megosztott kulcsos hitelesítés használatakor az elsődleges hozzáférési kulcs alapértelmezés szerint használatos.</span><span class="sxs-lookup"><span data-stu-id="d4b8f-123">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="d4b8f-124">A használni kívánt kulcs megváltoztatásához állítsa be a BatchAccountContext. KeyInUse tulajdonságot.</span><span class="sxs-lookup"><span data-stu-id="d4b8f-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="d4b8f-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4b8f-125">-DefaultProfile</span></span>
<span data-ttu-id="d4b8f-126">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d4b8f-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d4b8f-127">-Szűrő</span><span class="sxs-lookup"><span data-stu-id="d4b8f-127">-Filter</span></span>
<span data-ttu-id="d4b8f-128">Egy OData-szűrő záradékot ad meg.</span><span class="sxs-lookup"><span data-stu-id="d4b8f-128">Specifies an OData filter clause.</span></span>
<span data-ttu-id="d4b8f-129">Ha ezt a paramétert adja meg, ez a parancsmag a szűrőnek megfelelő tanúsítványokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="d4b8f-129">If you specify this parameter, this cmdlet gets the certificates that match the filter.</span></span>

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

### <span data-ttu-id="d4b8f-130">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="d4b8f-130">-MaxCount</span></span>
<span data-ttu-id="d4b8f-131">A visszaadni kívánt tanúsítványok maximális számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d4b8f-131">Specifies the maximum number of certificates to return.</span></span>
<span data-ttu-id="d4b8f-132">Ha a nulla (0) vagy annál kisebb értéket adja meg, a parancsmag nem használ felső határértéket.</span><span class="sxs-lookup"><span data-stu-id="d4b8f-132">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="d4b8f-133">Az alapértelmezett érték a 1000.</span><span class="sxs-lookup"><span data-stu-id="d4b8f-133">The default value is 1000.</span></span>

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

### <span data-ttu-id="d4b8f-134">-Válassza a</span><span class="sxs-lookup"><span data-stu-id="d4b8f-134">-Select</span></span>
<span data-ttu-id="d4b8f-135">Egy OData Select záradékot ad meg.</span><span class="sxs-lookup"><span data-stu-id="d4b8f-135">Specifies an OData select clause.</span></span>
<span data-ttu-id="d4b8f-136">Adjon meg egy értéket ehhez a paraméterhez, ha konkrét tulajdonságokat szeretne beszerezni az objektum összes tulajdonsága helyett.</span><span class="sxs-lookup"><span data-stu-id="d4b8f-136">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="d4b8f-137">-Ujjlenyomat</span><span class="sxs-lookup"><span data-stu-id="d4b8f-137">-Thumbprint</span></span>
<span data-ttu-id="d4b8f-138">Annak a tanúsítványnak az ujjlenyomatát adja meg, amely az adott parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="d4b8f-138">Specifies the thumbprint of the certificate that this cmdlet gets.</span></span>

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

### <span data-ttu-id="d4b8f-139">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="d4b8f-139">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="d4b8f-140">Az *ujjlenyomat* -paraméter származtatása algoritmust adja meg.</span><span class="sxs-lookup"><span data-stu-id="d4b8f-140">Specifies the algorithm used to derive the *Thumbprint* parameter.</span></span>
<span data-ttu-id="d4b8f-141">Jelenleg az egyetlen érvényes érték az SHA1.</span><span class="sxs-lookup"><span data-stu-id="d4b8f-141">Currently, the only valid value is sha1.</span></span>

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

### <span data-ttu-id="d4b8f-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4b8f-142">CommonParameters</span></span>
<span data-ttu-id="d4b8f-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d4b8f-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4b8f-144">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4b8f-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4b8f-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d4b8f-145">INPUTS</span></span>

### <span data-ttu-id="d4b8f-146">System. String</span><span class="sxs-lookup"><span data-stu-id="d4b8f-146">System.String</span></span>

### <span data-ttu-id="d4b8f-147">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="d4b8f-147">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="d4b8f-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d4b8f-148">OUTPUTS</span></span>

### <span data-ttu-id="d4b8f-149">Microsoft.Azure.Commands.BatCH. Modellek. PSCertificate</span><span class="sxs-lookup"><span data-stu-id="d4b8f-149">Microsoft.Azure.Commands.Batch.Models.PSCertificate</span></span>

## <span data-ttu-id="d4b8f-150">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d4b8f-150">NOTES</span></span>

## <span data-ttu-id="d4b8f-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d4b8f-151">RELATED LINKS</span></span>

[<span data-ttu-id="d4b8f-152">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="d4b8f-152">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="d4b8f-153">Új – AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="d4b8f-153">New-AzBatchCertificate</span></span>](./New-AzBatchCertificate.md)

[<span data-ttu-id="d4b8f-154">Remove-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="d4b8f-154">Remove-AzBatchCertificate</span></span>](./Remove-AzBatchCertificate.md)

[<span data-ttu-id="d4b8f-155">Azure-köteg parancsmagok</span><span class="sxs-lookup"><span data-stu-id="d4b8f-155">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


