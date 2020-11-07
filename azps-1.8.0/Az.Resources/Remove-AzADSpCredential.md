---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 04B1E3A6-6D52-46A3-8241-2CCDB5E71642
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azadspcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADSpCredential.md
ms.openlocfilehash: d40c1a3a5e626d364986352f95bc914b31ced969
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669354"
---
# <span data-ttu-id="24c02-101">Remove-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="24c02-101">Remove-AzADSpCredential</span></span>

## <span data-ttu-id="24c02-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="24c02-102">SYNOPSIS</span></span>
<span data-ttu-id="24c02-103">Hitelesítő adatok eltávolítása egy egyszerű szolgáltatótól.</span><span class="sxs-lookup"><span data-stu-id="24c02-103">Removes a credential from a service principal.</span></span>

## <span data-ttu-id="24c02-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="24c02-104">SYNTAX</span></span>

### <span data-ttu-id="24c02-105">ObjectIdWithKeyIdParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="24c02-105">ObjectIdWithKeyIdParameterSet (Default)</span></span>
```
Remove-AzADSpCredential -ObjectId <String> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24c02-106">SPNWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="24c02-106">SPNWithKeyIdParameterSet</span></span>
```
Remove-AzADSpCredential -ServicePrincipalName <String> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24c02-107">DisplayNameWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="24c02-107">DisplayNameWithKeyIdParameterSet</span></span>
```
Remove-AzADSpCredential -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24c02-108">ServicePrincipalObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="24c02-108">ServicePrincipalObjectParameterSet</span></span>
```
Remove-AzADSpCredential -ServicePrincipalObject <PSADServicePrincipal> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24c02-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="24c02-109">DESCRIPTION</span></span>
<span data-ttu-id="24c02-110">A Remove-AzADSpCredential parancsmag használatával kompromisszum vagy a hitelesítő adatok kulcsának lejárati dátuma részeként eltávolíthatja a hitelesítő adatok kulcsát a megbízótól.</span><span class="sxs-lookup"><span data-stu-id="24c02-110">The Remove-AzADSpCredential cmdlet can be used to remove a credential key from a service principal in the case of a compromise or as part of credential key rollover expiration.</span></span>
<span data-ttu-id="24c02-111">A rendszer az objektumazonosító vagy az egyszerű szolgáltatásnév (SPN) megadásával azonosítja a megbízót.</span><span class="sxs-lookup"><span data-stu-id="24c02-111">The service principal is identified by supplying either the object ID or service principal name (SPN).</span></span>
<span data-ttu-id="24c02-112">Az eltávolítani kívánt hitelesítő adatokat a program annak AZONOSÍTÓját azonosítja, ha az egyes hitelesítő adatok törlődnek, vagy egy "minden" kapcsolóval törli a szolgáltatóhoz társított összes hitelesítő adatokat.</span><span class="sxs-lookup"><span data-stu-id="24c02-112">The credential to be removed is identified by its key ID if an individual credential is to be removed or with an 'All' switch to delete all credentials associated with the service principal.</span></span>

## <span data-ttu-id="24c02-113">Példák</span><span class="sxs-lookup"><span data-stu-id="24c02-113">EXAMPLES</span></span>

### <span data-ttu-id="24c02-114">Példa 1 – meghatározott hitelesítő adatok eltávolítása egy egyszerű szolgáltatótól</span><span class="sxs-lookup"><span data-stu-id="24c02-114">Example 1 - Remove a specific credential from a service principal</span></span>

```
PS C:\> Remove-AzADSpCredential -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 -KeyId 9044423a-60a3-45ac-9ab1-09534157ebb
```

<span data-ttu-id="24c02-115">Eltávolítja a "9044423a-60a3-45ac-9ab1-09534157ebb" azonosítójú hitelesítő adatait a "7663d3fb-6f86-4352-9e6d-cf9d50d5ee82" azonosítójú.</span><span class="sxs-lookup"><span data-stu-id="24c02-115">Removes the credential with key id '9044423a-60a3-45ac-9ab1-09534157ebb' from the service principal with object id '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82'.</span></span>

### <span data-ttu-id="24c02-116">2. példa – minden hitelesítő adat eltávolítása egy egyszerű szolgáltatótól</span><span class="sxs-lookup"><span data-stu-id="24c02-116">Example 2 - Remove all credentials from a service principal</span></span>

```
PS C:\> Remove-AzADSpCredential -ServicePrincipalName http://test123
```

<span data-ttu-id="24c02-117">A szolgáltatás megbízójának összes hitelesítő adatait eltávolítja az SPN " http://test123 " értékkel.</span><span class="sxs-lookup"><span data-stu-id="24c02-117">Removes all credentials from the service principal with the SPN "http://test123".</span></span>

### <span data-ttu-id="24c02-118">3. példa – az összes hitelesítő adat eltávolítása a megbízótól csővezeték használatával</span><span class="sxs-lookup"><span data-stu-id="24c02-118">Example 3 - Remove all credentials from a service principal using piping</span></span>

```
PS C:\> Get-AzADServicePrincipal -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 | Remove-AzADSpCredential
```

<span data-ttu-id="24c02-119">A "7663d3fb-6f86-4352-9e6d-cf9d50d5ee82" azonosítójú objektumazonosítót és a Remove-AzADSpCredential parancsmagot tartalmazó csövekkel kapja meg a szolgáltatótól kapott összes hitelesítő adatok eltávolítását.</span><span class="sxs-lookup"><span data-stu-id="24c02-119">Gets the service principal with object id '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82' and pipes that to the Remove-AzADSpCredential cmdlet to remove all credentials from that service principal.</span></span>

## <span data-ttu-id="24c02-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="24c02-120">PARAMETERS</span></span>

### <span data-ttu-id="24c02-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24c02-121">-DefaultProfile</span></span>
<span data-ttu-id="24c02-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="24c02-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="24c02-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="24c02-123">-DisplayName</span></span>
<span data-ttu-id="24c02-124">A szolgáltatás megbízójának megjelenített neve.</span><span class="sxs-lookup"><span data-stu-id="24c02-124">The display name of the service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: DisplayNameWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24c02-125">-Force</span><span class="sxs-lookup"><span data-stu-id="24c02-125">-Force</span></span>
<span data-ttu-id="24c02-126">Váltás a hitelesítő adatok törlésére megerősítés nélkül.</span><span class="sxs-lookup"><span data-stu-id="24c02-126">Switch to delete credential without a confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24c02-127">-KeyId</span><span class="sxs-lookup"><span data-stu-id="24c02-127">-KeyId</span></span>
<span data-ttu-id="24c02-128">Az eltávolítandó hitelesítőadat-kulcsot adja meg.</span><span class="sxs-lookup"><span data-stu-id="24c02-128">Specifies the credential key to be removed.</span></span>
<span data-ttu-id="24c02-129">A megbízó kulcs-azonosítói a Get-AzADSpCredential parancsmag használatával szerezhetők be.</span><span class="sxs-lookup"><span data-stu-id="24c02-129">The key Ids for a service principal can be obtained using the Get-AzADSpCredential cmdlet.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ObjectIdWithKeyIdParameterSet, SPNWithKeyIdParameterSet, ServicePrincipalObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24c02-130">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="24c02-130">-ObjectId</span></span>
<span data-ttu-id="24c02-131">Annak az objektumnak az azonosítója a szolgáltatónál, akinek a hitelesítő adatait el szeretné távolítani.</span><span class="sxs-lookup"><span data-stu-id="24c02-131">The object id of the service principal to remove the credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: ObjectIdWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24c02-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="24c02-132">-PassThru</span></span>
<span data-ttu-id="24c02-133">Ez a beállítás akkor igaz, ha a parancs sikeres.</span><span class="sxs-lookup"><span data-stu-id="24c02-133">Specifying this will return true if the command was successful.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24c02-134">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="24c02-134">-ServicePrincipalName</span></span>
<span data-ttu-id="24c02-135">A szolgáltatás megbízójának neve (SPN) a hitelesítő adatok eltávolításához.</span><span class="sxs-lookup"><span data-stu-id="24c02-135">The name (SPN) of the service principal to remove the credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: SPNWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24c02-136">-ServicePrincipalObject</span><span class="sxs-lookup"><span data-stu-id="24c02-136">-ServicePrincipalObject</span></span>
<span data-ttu-id="24c02-137">A Service Principal objektum a hitelesítő adatok eltávolításához.</span><span class="sxs-lookup"><span data-stu-id="24c02-137">The service principal object to remove the credentials from.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal
Parameter Sets: ServicePrincipalObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="24c02-138">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="24c02-138">-Confirm</span></span>
<span data-ttu-id="24c02-139">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="24c02-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24c02-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24c02-140">-WhatIf</span></span>
<span data-ttu-id="24c02-141">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="24c02-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24c02-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="24c02-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24c02-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24c02-143">CommonParameters</span></span>
<span data-ttu-id="24c02-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="24c02-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24c02-145">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24c02-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24c02-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="24c02-146">INPUTS</span></span>

### <span data-ttu-id="24c02-147">System. String</span><span class="sxs-lookup"><span data-stu-id="24c02-147">System.String</span></span>

### <span data-ttu-id="24c02-148">Microsoft. Azure. Command. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="24c02-148">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

### <span data-ttu-id="24c02-149">System. GUID</span><span class="sxs-lookup"><span data-stu-id="24c02-149">System.Guid</span></span>

## <span data-ttu-id="24c02-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="24c02-150">OUTPUTS</span></span>

### <span data-ttu-id="24c02-151">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="24c02-151">System.Boolean</span></span>

## <span data-ttu-id="24c02-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="24c02-152">NOTES</span></span>

## <span data-ttu-id="24c02-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="24c02-153">RELATED LINKS</span></span>

[<span data-ttu-id="24c02-154">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="24c02-154">Get-AzADSpCredential</span></span>](./Get-AzADSpCredential.md)

[<span data-ttu-id="24c02-155">Új – AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="24c02-155">New-AzADSpCredential</span></span>](./New-AzADSpCredential.md)

[<span data-ttu-id="24c02-156">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="24c02-156">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

