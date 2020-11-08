---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 063BAA79-484D-48CF-9170-3808813752BD
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadspcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADSpCredential.md
ms.openlocfilehash: 46977fe6b2e6cf3c3811c7d9bbd49262b06cec54
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94017663"
---
# <span data-ttu-id="7ec49-101">New-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="7ec49-101">New-AzADSpCredential</span></span>

## <span data-ttu-id="7ec49-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7ec49-102">SYNOPSIS</span></span>
<span data-ttu-id="7ec49-103">Hitelesítő adatok hozzáadása egy meglévő szolgáltatási megbízóhoz.</span><span class="sxs-lookup"><span data-stu-id="7ec49-103">Adds a credential to an existing service principal.</span></span>

## <span data-ttu-id="7ec49-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7ec49-104">SYNTAX</span></span>

### <span data-ttu-id="7ec49-105">SpObjectIdWithPasswordParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7ec49-105">SpObjectIdWithPasswordParameterSet (Default)</span></span>
```
New-AzADSpCredential -ObjectId <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ec49-106">SpObjectIdWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="7ec49-106">SpObjectIdWithCertValueParameterSet</span></span>
```
New-AzADSpCredential -ObjectId <String> -CertValue <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ec49-107">SPNWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="7ec49-107">SPNWithCertValueParameterSet</span></span>
```
New-AzADSpCredential -ServicePrincipalName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ec49-108">SPNWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="7ec49-108">SPNWithPasswordParameterSet</span></span>
```
New-AzADSpCredential -ServicePrincipalName <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ec49-109">ServicePrincipalObjectWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="7ec49-109">ServicePrincipalObjectWithCertValueParameterSet</span></span>
```
New-AzADSpCredential -ServicePrincipalObject <PSADServicePrincipal> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ec49-110">ServicePrincipalObjectWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="7ec49-110">ServicePrincipalObjectWithPasswordParameterSet</span></span>
```
New-AzADSpCredential -ServicePrincipalObject <PSADServicePrincipal> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7ec49-111">Leírás</span><span class="sxs-lookup"><span data-stu-id="7ec49-111">DESCRIPTION</span></span>
<span data-ttu-id="7ec49-112">Az New-AzADSpCredential parancsmag használatával új hitelesítő adatokat vehet fel, illetve hitelesítő adatokat adhat meg a szolgáltatónál.</span><span class="sxs-lookup"><span data-stu-id="7ec49-112">The New-AzADSpCredential cmdlet can be used to add a new credential or to roll credentials for a service principal.</span></span>
<span data-ttu-id="7ec49-113">A szolgáltatás megbízóját az objektum-azonosító vagy a szolgáltatás egyszerű nevének ellátásával azonosítjuk.</span><span class="sxs-lookup"><span data-stu-id="7ec49-113">The service principal is identified by supplying either the object id or service principal name.</span></span>

## <span data-ttu-id="7ec49-114">Példák</span><span class="sxs-lookup"><span data-stu-id="7ec49-114">EXAMPLES</span></span>

### <span data-ttu-id="7ec49-115">Példa 1: új szolgáltatás elsődleges hitelesítő adatainak létrehozása generált jelszó használatával</span><span class="sxs-lookup"><span data-stu-id="7ec49-115">Example 1: Create a new service principal credential using a generated password</span></span>

```powershell
PS C:\> New-AzADSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476

Secret    : System.Security.SecureString
StartDate : 11/12/2018 9:36:05 PM
EndDate   : 11/12/2019 9:36:05 PM
KeyId     : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Type      : Password
```

<span data-ttu-id="7ec49-116">Az új jelszó-hitelesítő adatok a meglévő, a "1f99cf81-0146-4f4e-beae-2007d0668476" azonosítójú szolgáltatóhoz kerülnek.</span><span class="sxs-lookup"><span data-stu-id="7ec49-116">A new password credential is added to the existing service principal with object id '1f99cf81-0146-4f4e-beae-2007d0668476'.</span></span>

### <span data-ttu-id="7ec49-117">2. példa: új szolgáltatás-fő hitelesítő adatok létrehozása tanúsítvány használatával</span><span class="sxs-lookup"><span data-stu-id="7ec49-117">Example 2: Create a new service principal credential using a certificate</span></span>

```powershell
PS C:\> $cer = New-Object System.Security.Cryptography.X509Certificates.X509Certificate2
PS C:\> $cer.Import("C:\myapp.cer")
PS C:\> $binCert = $cer.GetRawCertData()
PS C:\> $credValue = [System.Convert]::ToBase64String($binCert)
PS C:\> New-AzADSpCredential -ServicePrincipalName "http://test123" -CertValue $credValue -StartDate $cer.NotBefore -EndDate $cer.NotAfter
```

<span data-ttu-id="7ec49-118">A megadott Base64-kódolt nyilvános X509 tanúsítvány ("SajátPr. cer") hozzáadódik a meglévő szolgáltatásnevet az SPN-lel.</span><span class="sxs-lookup"><span data-stu-id="7ec49-118">The supplied base64 encoded public X509 certificate ("myapp.cer") is added to the existing service principal using its SPN.</span></span>

### <span data-ttu-id="7ec49-119">3. példa: új szolgáltatás-fő hitelesítő adatok létrehozása csővezetékek használatával</span><span class="sxs-lookup"><span data-stu-id="7ec49-119">Example 3: Create a new service principal credential using piping</span></span>

```powershell
PS C:\> Get-AzADServicePrincipal -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 | New-AzADSpCredential

Secret    : System.Security.SecureString
StartDate : 11/12/2018 9:36:05 PM
EndDate   : 11/12/2019 9:36:05 PM
KeyId     : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Type      : Password
```

<span data-ttu-id="7ec49-120">Megkapja a "1f99cf81-0146-4f4e-beae-2007d0668476" azonosítójú szolgáltatásnevet, valamint a New-AzADSpCredential csöveket, amelyekkel létrehozhatja az új szolgáltatás-fő hitelesítő adatait a szolgáltatónál egy generált jelszóval.</span><span class="sxs-lookup"><span data-stu-id="7ec49-120">Gets the service principal with object id '1f99cf81-0146-4f4e-beae-2007d0668476' and pipes that to the New-AzADSpCredential to create a new service principal credential for that service principal with a generated password.</span></span>

## <span data-ttu-id="7ec49-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7ec49-121">PARAMETERS</span></span>

### <span data-ttu-id="7ec49-122">-CertValue</span><span class="sxs-lookup"><span data-stu-id="7ec49-122">-CertValue</span></span>
<span data-ttu-id="7ec49-123">Az "aszimmetrikus" hitelesítőadat-típus értéke.</span><span class="sxs-lookup"><span data-stu-id="7ec49-123">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="7ec49-124">A 64 kódolt tanúsítványát jelöli.</span><span class="sxs-lookup"><span data-stu-id="7ec49-124">It represents the base 64 encoded certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: SpObjectIdWithCertValueParameterSet, SPNWithCertValueParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ServicePrincipalObjectWithCertValueParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ec49-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ec49-125">-DefaultProfile</span></span>
<span data-ttu-id="7ec49-126">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="7ec49-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7ec49-127">-EndDate</span><span class="sxs-lookup"><span data-stu-id="7ec49-127">-EndDate</span></span>
<span data-ttu-id="7ec49-128">A hitelesítő adatok használatának tényleges befejezési dátuma.</span><span class="sxs-lookup"><span data-stu-id="7ec49-128">The effective end date of the credential usage.</span></span>
<span data-ttu-id="7ec49-129">Az alapértelmezett befejezési dátum értéke egy év a mai naptól számítva.</span><span class="sxs-lookup"><span data-stu-id="7ec49-129">The default end date value is one year from today.</span></span>
<span data-ttu-id="7ec49-130">Ha "aszimmetrikus" típusú hitelesítő adatokra van szükség, ezt a X509 tanúsítvány érvényességi dátumának be vagy ki kell állítania.</span><span class="sxs-lookup"><span data-stu-id="7ec49-130">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ec49-131">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="7ec49-131">-ObjectId</span></span>
<span data-ttu-id="7ec49-132">Annak az objektumnak az azonosítója a szolgáltatónál, akinek a hitelesítő adatait hozzá szeretné adni.</span><span class="sxs-lookup"><span data-stu-id="7ec49-132">The object id of the service principal to add the credentials to.</span></span>

```yaml
Type: System.String
Parameter Sets: SpObjectIdWithPasswordParameterSet, SpObjectIdWithCertValueParameterSet
Aliases: ServicePrincipalObjectId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ec49-133">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="7ec49-133">-ServicePrincipalName</span></span>
<span data-ttu-id="7ec49-134">Annak a szolgáltatónak a neve (SPN), amelyhez hozzá szeretné adni a hitelesítő adatokat.</span><span class="sxs-lookup"><span data-stu-id="7ec49-134">The name (SPN) of the service principal to add the credentials to.</span></span>

```yaml
Type: System.String
Parameter Sets: SPNWithCertValueParameterSet, SPNWithPasswordParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ec49-135">-ServicePrincipalObject</span><span class="sxs-lookup"><span data-stu-id="7ec49-135">-ServicePrincipalObject</span></span>
<span data-ttu-id="7ec49-136">A Service Principal objektum a hitelesítő adatok hozzáadásához.</span><span class="sxs-lookup"><span data-stu-id="7ec49-136">The service principal object to add the credentials to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal
Parameter Sets: ServicePrincipalObjectWithCertValueParameterSet, ServicePrincipalObjectWithPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7ec49-137">-StartDate</span><span class="sxs-lookup"><span data-stu-id="7ec49-137">-StartDate</span></span>
<span data-ttu-id="7ec49-138">A hitelesítő adatok használatának tényleges kezdési dátuma.</span><span class="sxs-lookup"><span data-stu-id="7ec49-138">The effective start date of the credential usage.</span></span>
<span data-ttu-id="7ec49-139">A kezdő dátum alapértelmezett értéke ma.</span><span class="sxs-lookup"><span data-stu-id="7ec49-139">The default start date value is today.</span></span>
<span data-ttu-id="7ec49-140">Ha "aszimmetrikus" típusú hitelesítő adatokra van szükség, ezt a X509-tanúsítvány érvényességi dátumának be vagy mögé kell állítani.</span><span class="sxs-lookup"><span data-stu-id="7ec49-140">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ec49-141">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7ec49-141">-Confirm</span></span>
<span data-ttu-id="7ec49-142">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7ec49-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ec49-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ec49-143">-WhatIf</span></span>
<span data-ttu-id="7ec49-144">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7ec49-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ec49-145">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7ec49-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ec49-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ec49-146">CommonParameters</span></span>
<span data-ttu-id="7ec49-147">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7ec49-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ec49-148">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="7ec49-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ec49-149">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7ec49-149">INPUTS</span></span>

### <span data-ttu-id="7ec49-150">System. String</span><span class="sxs-lookup"><span data-stu-id="7ec49-150">System.String</span></span>

### <span data-ttu-id="7ec49-151">Microsoft. Azure. Command. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="7ec49-151">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

### <span data-ttu-id="7ec49-152">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="7ec49-152">System.DateTime</span></span>

## <span data-ttu-id="7ec49-153">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7ec49-153">OUTPUTS</span></span>

### <span data-ttu-id="7ec49-154">Microsoft. Azure. Command. ActiveDirectory. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="7ec49-154">Microsoft.Azure.Commands.ActiveDirectory.PSADCredential</span></span>

### <span data-ttu-id="7ec49-155">Microsoft. Azure. Command. Resources. modellek. Authorization. PSADCredentialWrapper</span><span class="sxs-lookup"><span data-stu-id="7ec49-155">Microsoft.Azure.Commands.Resources.Models.Authorization.PSADCredentialWrapper</span></span>

## <span data-ttu-id="7ec49-156">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7ec49-156">NOTES</span></span>

## <span data-ttu-id="7ec49-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7ec49-157">RELATED LINKS</span></span>

[<span data-ttu-id="7ec49-158">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="7ec49-158">Get-AzADSpCredential</span></span>](./Get-AzADSpCredential.md)

[<span data-ttu-id="7ec49-159">Remove-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="7ec49-159">Remove-AzADSpCredential</span></span>](./Remove-AzADSpCredential.md)

[<span data-ttu-id="7ec49-160">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="7ec49-160">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)



