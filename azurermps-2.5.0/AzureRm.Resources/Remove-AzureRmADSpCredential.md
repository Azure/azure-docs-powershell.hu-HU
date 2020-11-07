---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 04B1E3A6-6D52-46A3-8241-2CCDB5E71642
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermadspcredential
schema: 2.0.0
ms.openlocfilehash: 73fff5ff4cf612c39bacd26fed61c4e856e34128
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848098"
---
# <span data-ttu-id="8e722-101">Remove-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="8e722-101">Remove-AzureRmADSpCredential</span></span>

## <span data-ttu-id="8e722-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8e722-102">SYNOPSIS</span></span>
<span data-ttu-id="8e722-103">Hitelesítő adatok eltávolítása egy egyszerű szolgáltatótól.</span><span class="sxs-lookup"><span data-stu-id="8e722-103">Removes a credential from a service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8e722-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8e722-104">SYNTAX</span></span>

### <span data-ttu-id="8e722-105">ObjectIdWithKeyIdParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8e722-105">ObjectIdWithKeyIdParameterSet (Default)</span></span>
```
Remove-AzureRmADSpCredential -ObjectId <Guid> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e722-106">SPNWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e722-106">SPNWithKeyIdParameterSet</span></span>
```
Remove-AzureRmADSpCredential -ServicePrincipalName <String> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e722-107">DisplayNameWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e722-107">DisplayNameWithKeyIdParameterSet</span></span>
```
Remove-AzureRmADSpCredential -DisplayName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e722-108">ServicePrincipalObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e722-108">ServicePrincipalObjectParameterSet</span></span>
```
Remove-AzureRmADSpCredential -ServicePrincipalObject <PSADServicePrincipal> [-KeyId <Guid>] [-PassThru]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e722-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="8e722-109">DESCRIPTION</span></span>
<span data-ttu-id="8e722-110">A Remove-AzureRmADSpCredential parancsmag használatával kompromisszum vagy a hitelesítő adatok kulcsának lejárati dátuma részeként eltávolíthatja a hitelesítő adatok kulcsát a megbízótól.</span><span class="sxs-lookup"><span data-stu-id="8e722-110">The Remove-AzureRmADSpCredential cmdlet can be used to remove a credential key from a service principal in the case of a compromise or as part of credential key rollover expiration.</span></span>
<span data-ttu-id="8e722-111">A rendszer az objektumazonosító vagy az egyszerű szolgáltatásnév (SPN) megadásával azonosítja a megbízót.</span><span class="sxs-lookup"><span data-stu-id="8e722-111">The service principal is identified by supplying either the object ID or service principal name (SPN).</span></span>
<span data-ttu-id="8e722-112">Az eltávolítani kívánt hitelesítő adatokat a program annak AZONOSÍTÓját azonosítja, ha az egyes hitelesítő adatok törlődnek, vagy egy "minden" kapcsolóval törli a szolgáltatóhoz társított összes hitelesítő adatokat.</span><span class="sxs-lookup"><span data-stu-id="8e722-112">The credential to be removed is identified by its key ID if an individual credential is to be removed or with an 'All' switch to delete all credentials associated with the service principal.</span></span>

## <span data-ttu-id="8e722-113">Példák</span><span class="sxs-lookup"><span data-stu-id="8e722-113">EXAMPLES</span></span>

### <span data-ttu-id="8e722-114">Példa 1 – meghatározott hitelesítő adatok eltávolítása egy egyszerű szolgáltatótól</span><span class="sxs-lookup"><span data-stu-id="8e722-114">Example 1 - Remove a specific credential from a service principal</span></span>

```
PS C:\> Remove-AzureRmADSpCredential -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 -KeyId 9044423a-60a3-45ac-9ab1-09534157ebb
```

<span data-ttu-id="8e722-115">Eltávolítja a "9044423a-60a3-45ac-9ab1-09534157ebb" azonosítójú hitelesítő adatait a "7663d3fb-6f86-4352-9e6d-cf9d50d5ee82" azonosítójú.</span><span class="sxs-lookup"><span data-stu-id="8e722-115">Removes the credential with key id '9044423a-60a3-45ac-9ab1-09534157ebb' from the service principal with object id '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82'.</span></span>

### <span data-ttu-id="8e722-116">2. példa – minden hitelesítő adat eltávolítása egy egyszerű szolgáltatótól</span><span class="sxs-lookup"><span data-stu-id="8e722-116">Example 2 - Remove all credentials from a service principal</span></span>

```
PS C:\> Remove-AzureRmADSpCredential -ServicePrincipalName http://test123
```

<span data-ttu-id="8e722-117">A szolgáltatás megbízójának összes hitelesítő adatait eltávolítja az SPN " http://test123 " értékkel.</span><span class="sxs-lookup"><span data-stu-id="8e722-117">Removes all credentials from the service principal with the SPN "http://test123".</span></span>

### <span data-ttu-id="8e722-118">3. példa – az összes hitelesítő adat eltávolítása a megbízótól csővezeték használatával</span><span class="sxs-lookup"><span data-stu-id="8e722-118">Example 3 - Remove all credentials from a service principal using piping</span></span>

```
PS C:\> Get-AzureRmADServicePrincipal -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 | Remove-AzureRmADSpCredential
```

<span data-ttu-id="8e722-119">A "7663d3fb-6f86-4352-9e6d-cf9d50d5ee82" azonosítójú objektumazonosítót és a Remove-AzureRmADSpCredential parancsmagot tartalmazó csövekkel kapja meg a szolgáltatótól kapott összes hitelesítő adatok eltávolítását.</span><span class="sxs-lookup"><span data-stu-id="8e722-119">Gets the service principal with object id '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82' and pipes that to the Remove-AzureRmADSpCredential cmdlet to remove all credentials from that service principal.</span></span>

## <span data-ttu-id="8e722-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8e722-120">PARAMETERS</span></span>

### <span data-ttu-id="8e722-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e722-121">-DefaultProfile</span></span>
<span data-ttu-id="8e722-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="8e722-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e722-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="8e722-123">-DisplayName</span></span>
<span data-ttu-id="8e722-124">A szolgáltatás megbízójának megjelenített neve.</span><span class="sxs-lookup"><span data-stu-id="8e722-124">The display name of the service principal.</span></span>

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

### <span data-ttu-id="8e722-125">-Force</span><span class="sxs-lookup"><span data-stu-id="8e722-125">-Force</span></span>
<span data-ttu-id="8e722-126">Váltás a hitelesítő adatok törlésére megerősítés nélkül.</span><span class="sxs-lookup"><span data-stu-id="8e722-126">Switch to delete credential without a confirmation.</span></span>

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

### <span data-ttu-id="8e722-127">-KeyId</span><span class="sxs-lookup"><span data-stu-id="8e722-127">-KeyId</span></span>
<span data-ttu-id="8e722-128">Az eltávolítandó hitelesítőadat-kulcsot adja meg.</span><span class="sxs-lookup"><span data-stu-id="8e722-128">Specifies the credential key to be removed.</span></span>
<span data-ttu-id="8e722-129">A megbízó kulcs-azonosítói a Get-AzureRmADSpCredential parancsmag használatával szerezhetők be.</span><span class="sxs-lookup"><span data-stu-id="8e722-129">The key Ids for a service principal can be obtained using the Get-AzureRmADSpCredential cmdlet.</span></span>

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

### <span data-ttu-id="8e722-130">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="8e722-130">-ObjectId</span></span>
<span data-ttu-id="8e722-131">Annak az objektumnak az azonosítója a szolgáltatónál, akinek a hitelesítő adatait el szeretné távolítani.</span><span class="sxs-lookup"><span data-stu-id="8e722-131">The object id of the service principal to remove the credentials from.</span></span>

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

### <span data-ttu-id="8e722-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8e722-132">-PassThru</span></span>
<span data-ttu-id="8e722-133">Ez a beállítás akkor igaz, ha a parancs sikeres.</span><span class="sxs-lookup"><span data-stu-id="8e722-133">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="8e722-134">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="8e722-134">-ServicePrincipalName</span></span>
<span data-ttu-id="8e722-135">A szolgáltatás megbízójának neve (SPN) a hitelesítő adatok eltávolításához.</span><span class="sxs-lookup"><span data-stu-id="8e722-135">The name (SPN) of the service principal to remove the credentials from.</span></span>

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

### <span data-ttu-id="8e722-136">-ServicePrincipalObject</span><span class="sxs-lookup"><span data-stu-id="8e722-136">-ServicePrincipalObject</span></span>
<span data-ttu-id="8e722-137">A Service Principal objektum a hitelesítő adatok eltávolításához.</span><span class="sxs-lookup"><span data-stu-id="8e722-137">The service principal object to remove the credentials from.</span></span>

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

### <span data-ttu-id="8e722-138">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="8e722-138">-Confirm</span></span>
<span data-ttu-id="8e722-139">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="8e722-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e722-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e722-140">-WhatIf</span></span>
<span data-ttu-id="8e722-141">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="8e722-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e722-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8e722-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e722-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e722-143">CommonParameters</span></span>
<span data-ttu-id="8e722-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8e722-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e722-145">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e722-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e722-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8e722-146">INPUTS</span></span>

### <span data-ttu-id="8e722-147">System. GUID</span><span class="sxs-lookup"><span data-stu-id="8e722-147">System.Guid</span></span>

### <span data-ttu-id="8e722-148">System. String</span><span class="sxs-lookup"><span data-stu-id="8e722-148">System.String</span></span>

### <span data-ttu-id="8e722-149">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="8e722-149">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>
<span data-ttu-id="8e722-150">Paraméterek: ServicePrincipalObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="8e722-150">Parameters: ServicePrincipalObject (ByValue)</span></span>

## <span data-ttu-id="8e722-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8e722-151">OUTPUTS</span></span>

### <span data-ttu-id="8e722-152">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8e722-152">System.Boolean</span></span>

## <span data-ttu-id="8e722-153">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8e722-153">NOTES</span></span>

## <span data-ttu-id="8e722-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8e722-154">RELATED LINKS</span></span>

[<span data-ttu-id="8e722-155">Get-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="8e722-155">Get-AzureRmADSpCredential</span></span>](./Get-AzureRmADSpCredential.md)

[<span data-ttu-id="8e722-156">Új – AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="8e722-156">New-AzureRmADSpCredential</span></span>](./New-AzureRmADSpCredential.md)

[<span data-ttu-id="8e722-157">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="8e722-157">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

