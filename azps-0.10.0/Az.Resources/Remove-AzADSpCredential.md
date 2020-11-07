---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 04B1E3A6-6D52-46A3-8241-2CCDB5E71642
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-Azadspcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzADSpCredential.md
ms.openlocfilehash: 39796e1e9d77fb95c65b7ac72e9dee3ee266af10
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843277"
---
# <span data-ttu-id="c174e-101">Remove-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="c174e-101">Remove-AzADSpCredential</span></span>

## <span data-ttu-id="c174e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c174e-102">SYNOPSIS</span></span>
<span data-ttu-id="c174e-103">Hitelesítő adatok eltávolítása egy egyszerű szolgáltatótól.</span><span class="sxs-lookup"><span data-stu-id="c174e-103">Removes a credential from a service principal.</span></span>

## <span data-ttu-id="c174e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c174e-104">SYNTAX</span></span>

### <span data-ttu-id="c174e-105">ObjectIdWithKeyIdParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c174e-105">ObjectIdWithKeyIdParameterSet (Default)</span></span>
```
Remove-AzADSpCredential -ObjectId <Guid> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c174e-106">SPNWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c174e-106">SPNWithKeyIdParameterSet</span></span>
```
Remove-AzADSpCredential -ServicePrincipalName <String> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c174e-107">DisplayNameWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c174e-107">DisplayNameWithKeyIdParameterSet</span></span>
```
Remove-AzADSpCredential -DisplayName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c174e-108">ServicePrincipalObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c174e-108">ServicePrincipalObjectParameterSet</span></span>
```
Remove-AzADSpCredential -ServicePrincipalObject <PSADServicePrincipal> [-KeyId <Guid>] [-PassThru]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c174e-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="c174e-109">DESCRIPTION</span></span>
<span data-ttu-id="c174e-110">A Remove-AzADSpCredential parancsmag használatával kompromisszum vagy a hitelesítő adatok kulcsának lejárati dátuma részeként eltávolíthatja a hitelesítő adatok kulcsát a megbízótól.</span><span class="sxs-lookup"><span data-stu-id="c174e-110">The Remove-AzADSpCredential cmdlet can be used to remove a credential key from a service principal in the case of a compromise or as part of credential key rollover expiration.</span></span>
<span data-ttu-id="c174e-111">A rendszer az objektumazonosító vagy az egyszerű szolgáltatásnév (SPN) megadásával azonosítja a megbízót.</span><span class="sxs-lookup"><span data-stu-id="c174e-111">The service principal is identified by supplying either the object ID or service principal name (SPN).</span></span>
<span data-ttu-id="c174e-112">Az eltávolítani kívánt hitelesítő adatokat a program annak AZONOSÍTÓját azonosítja, ha az egyes hitelesítő adatok törlődnek, vagy egy "minden" kapcsolóval törli a szolgáltatóhoz társított összes hitelesítő adatokat.</span><span class="sxs-lookup"><span data-stu-id="c174e-112">The credential to be removed is identified by its key ID if an individual credential is to be removed or with an 'All' switch to delete all credentials associated with the service principal.</span></span>

## <span data-ttu-id="c174e-113">Példák</span><span class="sxs-lookup"><span data-stu-id="c174e-113">EXAMPLES</span></span>

### <span data-ttu-id="c174e-114">Példa 1 – meghatározott hitelesítő adatok eltávolítása egy egyszerű szolgáltatótól</span><span class="sxs-lookup"><span data-stu-id="c174e-114">Example 1 - Remove a specific credential from a service principal</span></span>

```
PS C:\> Remove-AzADSpCredential -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 -KeyId 9044423a-60a3-45ac-9ab1-09534157ebb
```

<span data-ttu-id="c174e-115">Eltávolítja a "9044423a-60a3-45ac-9ab1-09534157ebb" azonosítójú hitelesítő adatait a "7663d3fb-6f86-4352-9e6d-cf9d50d5ee82" azonosítójú.</span><span class="sxs-lookup"><span data-stu-id="c174e-115">Removes the credential with key id '9044423a-60a3-45ac-9ab1-09534157ebb' from the service principal with object id '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82'.</span></span>

### <span data-ttu-id="c174e-116">2. példa – minden hitelesítő adat eltávolítása egy egyszerű szolgáltatótól</span><span class="sxs-lookup"><span data-stu-id="c174e-116">Example 2 - Remove all credentials from a service principal</span></span>

```
PS C:\> Remove-AzADSpCredential -ServicePrincipalName http://test123
```

<span data-ttu-id="c174e-117">A szolgáltatás megbízójának összes hitelesítő adatait eltávolítja az SPN " http://test123 " értékkel.</span><span class="sxs-lookup"><span data-stu-id="c174e-117">Removes all credentials from the service principal with the SPN "http://test123".</span></span>

### <span data-ttu-id="c174e-118">3. példa – az összes hitelesítő adat eltávolítása a megbízótól csővezeték használatával</span><span class="sxs-lookup"><span data-stu-id="c174e-118">Example 3 - Remove all credentials from a service principal using piping</span></span>

```
PS C:\> Get-AzADServicePrincipal -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 | Remove-AzADSpCredential
```

<span data-ttu-id="c174e-119">A "7663d3fb-6f86-4352-9e6d-cf9d50d5ee82" azonosítójú objektumazonosítót és a Remove-AzADSpCredential parancsmagot tartalmazó csövekkel kapja meg a szolgáltatótól kapott összes hitelesítő adatok eltávolítását.</span><span class="sxs-lookup"><span data-stu-id="c174e-119">Gets the service principal with object id '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82' and pipes that to the Remove-AzADSpCredential cmdlet to remove all credentials from that service principal.</span></span>

## <span data-ttu-id="c174e-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c174e-120">PARAMETERS</span></span>

### <span data-ttu-id="c174e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c174e-121">-DefaultProfile</span></span>
<span data-ttu-id="c174e-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="c174e-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c174e-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="c174e-123">-DisplayName</span></span>
<span data-ttu-id="c174e-124">A szolgáltatás megbízójának megjelenített neve.</span><span class="sxs-lookup"><span data-stu-id="c174e-124">The display name of the service principal.</span></span>

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

### <span data-ttu-id="c174e-125">-Force</span><span class="sxs-lookup"><span data-stu-id="c174e-125">-Force</span></span>
<span data-ttu-id="c174e-126">Váltás a hitelesítő adatok törlésére megerősítés nélkül.</span><span class="sxs-lookup"><span data-stu-id="c174e-126">Switch to delete credential without a confirmation.</span></span>

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

### <span data-ttu-id="c174e-127">-KeyId</span><span class="sxs-lookup"><span data-stu-id="c174e-127">-KeyId</span></span>
<span data-ttu-id="c174e-128">Az eltávolítandó hitelesítőadat-kulcsot adja meg.</span><span class="sxs-lookup"><span data-stu-id="c174e-128">Specifies the credential key to be removed.</span></span>
<span data-ttu-id="c174e-129">A megbízó kulcs-azonosítói a Get-AzADSpCredential parancsmag használatával szerezhetők be.</span><span class="sxs-lookup"><span data-stu-id="c174e-129">The key Ids for a service principal can be obtained using the Get-AzADSpCredential cmdlet.</span></span>

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

### <span data-ttu-id="c174e-130">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="c174e-130">-ObjectId</span></span>
<span data-ttu-id="c174e-131">Annak az objektumnak az azonosítója a szolgáltatónál, akinek a hitelesítő adatait el szeretné távolítani.</span><span class="sxs-lookup"><span data-stu-id="c174e-131">The object id of the service principal to remove the credentials from.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ObjectIdWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c174e-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c174e-132">-PassThru</span></span>
<span data-ttu-id="c174e-133">Ez a beállítás akkor igaz, ha a parancs sikeres.</span><span class="sxs-lookup"><span data-stu-id="c174e-133">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="c174e-134">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="c174e-134">-ServicePrincipalName</span></span>
<span data-ttu-id="c174e-135">A szolgáltatás megbízójának neve (SPN) a hitelesítő adatok eltávolításához.</span><span class="sxs-lookup"><span data-stu-id="c174e-135">The name (SPN) of the service principal to remove the credentials from.</span></span>

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

### <span data-ttu-id="c174e-136">-ServicePrincipalObject</span><span class="sxs-lookup"><span data-stu-id="c174e-136">-ServicePrincipalObject</span></span>
<span data-ttu-id="c174e-137">A Service Principal objektum a hitelesítő adatok eltávolításához.</span><span class="sxs-lookup"><span data-stu-id="c174e-137">The service principal object to remove the credentials from.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal
Parameter Sets: ServicePrincipalObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c174e-138">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c174e-138">-Confirm</span></span>
<span data-ttu-id="c174e-139">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c174e-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c174e-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c174e-140">-WhatIf</span></span>
<span data-ttu-id="c174e-141">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c174e-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c174e-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c174e-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c174e-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c174e-143">CommonParameters</span></span>
<span data-ttu-id="c174e-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c174e-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c174e-145">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c174e-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c174e-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c174e-146">INPUTS</span></span>

### <span data-ttu-id="c174e-147">System. GUID</span><span class="sxs-lookup"><span data-stu-id="c174e-147">System.Guid</span></span>

### <span data-ttu-id="c174e-148">System. String</span><span class="sxs-lookup"><span data-stu-id="c174e-148">System.String</span></span>

### <span data-ttu-id="c174e-149">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="c174e-149">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>
<span data-ttu-id="c174e-150">Paraméterek: ServicePrincipalObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c174e-150">Parameters: ServicePrincipalObject (ByValue)</span></span>

## <span data-ttu-id="c174e-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c174e-151">OUTPUTS</span></span>

### <span data-ttu-id="c174e-152">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c174e-152">System.Boolean</span></span>

## <span data-ttu-id="c174e-153">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c174e-153">NOTES</span></span>

## <span data-ttu-id="c174e-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c174e-154">RELATED LINKS</span></span>

[<span data-ttu-id="c174e-155">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="c174e-155">Get-AzADSpCredential</span></span>](./Get-AzADSpCredential.md)

[<span data-ttu-id="c174e-156">Új – AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="c174e-156">New-AzADSpCredential</span></span>](./New-AzADSpCredential.md)

[<span data-ttu-id="c174e-157">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="c174e-157">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

