---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C61FA834-BEBE-4DBF-888F-C6CB8CC95390
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azadappcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADAppCredential.md
ms.openlocfilehash: 5c47e707c3421c6efc1998e55897f6bb9be8fa65
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669363"
---
# <span data-ttu-id="9fe28-101">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="9fe28-101">Remove-AzADAppCredential</span></span>

## <span data-ttu-id="9fe28-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9fe28-102">SYNOPSIS</span></span>
<span data-ttu-id="9fe28-103">Hitelesítő adatok eltávolítása egy alkalmazásból.</span><span class="sxs-lookup"><span data-stu-id="9fe28-103">Removes a credential from an application.</span></span>

## <span data-ttu-id="9fe28-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9fe28-104">SYNTAX</span></span>

### <span data-ttu-id="9fe28-105">ApplicationObjectIdWithKeyIdParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9fe28-105">ApplicationObjectIdWithKeyIdParameterSet (Default)</span></span>
```
Remove-AzADAppCredential -ObjectId <String> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9fe28-106">ApplicationIdWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9fe28-106">ApplicationIdWithKeyIdParameterSet</span></span>
```
Remove-AzADAppCredential -ApplicationId <Guid> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9fe28-107">ApplicationDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9fe28-107">ApplicationDisplayNameParameterSet</span></span>
```
Remove-AzADAppCredential -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9fe28-108">ApplicationObjectWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9fe28-108">ApplicationObjectWithKeyIdParameterSet</span></span>
```
Remove-AzADAppCredential [-KeyId <Guid>] -ApplicationObject <PSADApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9fe28-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="9fe28-109">DESCRIPTION</span></span>
<span data-ttu-id="9fe28-110">A Remove-AzADAppCredential parancsmagot kiegyezéssel vagy a hitelesítő adatok kulcsának lejárati időpontjának részeként lehet eltávolítani egy alkalmazás hitelesítő kulcsával.</span><span class="sxs-lookup"><span data-stu-id="9fe28-110">The Remove-AzADAppCredential cmdlet can be used to remove a credential key from an application in the case of a compromise or as part of credential key rollover expiration.</span></span>
<span data-ttu-id="9fe28-111">Az alkalmazás azonosítása az objektum-azonosító vagy a AppId megadásával történik.</span><span class="sxs-lookup"><span data-stu-id="9fe28-111">The application is identified by supplying either the object ID or AppId.</span></span>
<span data-ttu-id="9fe28-112">Az eltávolítandó hitelesítő adatok azonosítása a kulcs azonosítója alapján történik.</span><span class="sxs-lookup"><span data-stu-id="9fe28-112">The credential to be removed is identified by its key ID.</span></span>

## <span data-ttu-id="9fe28-113">Példák</span><span class="sxs-lookup"><span data-stu-id="9fe28-113">EXAMPLES</span></span>

### <span data-ttu-id="9fe28-114">Példa 1 – meghatározott hitelesítő adatok eltávolítása egy alkalmazásból</span><span class="sxs-lookup"><span data-stu-id="9fe28-114">Example 1 - Remove a specific credential from an application</span></span>

```
PS C:\> Remove-AzADAppCredential -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 -KeyId 9044423a-60a3-45ac-9ab1-09534157ebb
```

<span data-ttu-id="9fe28-115">Eltávolítja a "9044423a-60a3-45ac-9ab1-09534157ebb" azonosítójú hitelesítő adatokat a "7663d3fb-6f86-4352-9e6d-cf9d50d5ee82" azonosítójú alkalmazásból.</span><span class="sxs-lookup"><span data-stu-id="9fe28-115">Removes the credential with key id '9044423a-60a3-45ac-9ab1-09534157ebb' from the application with object id '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82'.</span></span>

### <span data-ttu-id="9fe28-116">2. példa – az összes hitelesítő adat eltávolítása egy alkalmazásból</span><span class="sxs-lookup"><span data-stu-id="9fe28-116">Example 2 - Remove all credentials from an application</span></span>

```
PS C:\> Remove-AzADAppCredential -ApplicationId 4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58
```

<span data-ttu-id="9fe28-117">A "4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58" azonosítójú alkalmazásban az összes hitelesítő adat eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="9fe28-117">Removes all credentials from the application with application id '4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58'.</span></span>

### <span data-ttu-id="9fe28-118">3 példa – az összes hitelesítő adat eltávolítása a csővezetékekkel</span><span class="sxs-lookup"><span data-stu-id="9fe28-118">Example 3 - Remove all credentials using piping</span></span>

```
PS C:\> Get-AzADApplication -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 | Remove-AzADAppCredential
```

<span data-ttu-id="9fe28-119">Beilleszti az alkalmazást a "7663d3fb-6f86-4352-9e6d-cf9d50d5ee82" azonosítójú objektumazonosítót, valamint az Remove-AzADAppCredential parancsmaghoz tartozó csöveket, és eltávolítja az adott alkalmazás összes hitelesítő adatait.</span><span class="sxs-lookup"><span data-stu-id="9fe28-119">Gets the application with object id '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82' and pipes that to the Remove-AzADAppCredential cmdlet and removes all credentials from that application.</span></span>

## <span data-ttu-id="9fe28-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9fe28-120">PARAMETERS</span></span>

### <span data-ttu-id="9fe28-121">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="9fe28-121">-ApplicationId</span></span>
<span data-ttu-id="9fe28-122">Az alkalmazás azonosítója a hitelesítő adatok eltávolításához.</span><span class="sxs-lookup"><span data-stu-id="9fe28-122">The id of the application to remove the credentials from.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationIdWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fe28-123">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="9fe28-123">-ApplicationObject</span></span>
<span data-ttu-id="9fe28-124">Az Application objektum a hitelesítő adatok eltávolításához.</span><span class="sxs-lookup"><span data-stu-id="9fe28-124">The application object to remove the credentials from.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9fe28-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fe28-125">-DefaultProfile</span></span>
<span data-ttu-id="9fe28-126">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="9fe28-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9fe28-127">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="9fe28-127">-DisplayName</span></span>
<span data-ttu-id="9fe28-128">Az alkalmazás megjelenítendő neve.</span><span class="sxs-lookup"><span data-stu-id="9fe28-128">The display name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationDisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fe28-129">-Force</span><span class="sxs-lookup"><span data-stu-id="9fe28-129">-Force</span></span>
<span data-ttu-id="9fe28-130">Váltás a hitelesítő adatok törlésére megerősítés nélkül.</span><span class="sxs-lookup"><span data-stu-id="9fe28-130">Switch to delete credential without a confirmation.</span></span>

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

### <span data-ttu-id="9fe28-131">-KeyId</span><span class="sxs-lookup"><span data-stu-id="9fe28-131">-KeyId</span></span>
<span data-ttu-id="9fe28-132">Az eltávolítandó hitelesítőadat-kulcsot adja meg.</span><span class="sxs-lookup"><span data-stu-id="9fe28-132">Specifies the credential key to be removed.</span></span>
<span data-ttu-id="9fe28-133">Az alkalmazáshoz tartozó kulcs-azonosítók az Get-AzADAppCredential parancsmag használatával szerezhetők be.</span><span class="sxs-lookup"><span data-stu-id="9fe28-133">The key Ids for the application can be obtained using the Get-AzADAppCredential cmdlet.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationObjectIdWithKeyIdParameterSet, ApplicationIdWithKeyIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Guid
Parameter Sets: ApplicationObjectWithKeyIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fe28-134">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="9fe28-134">-ObjectId</span></span>
<span data-ttu-id="9fe28-135">Az alkalmazás Object ID-je a hitelesítő adatok eltávolításához.</span><span class="sxs-lookup"><span data-stu-id="9fe28-135">The object id of the application to remove the credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationObjectIdWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fe28-136">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9fe28-136">-PassThru</span></span>
<span data-ttu-id="9fe28-137">Ez a beállítás akkor igaz, ha a parancs sikeres.</span><span class="sxs-lookup"><span data-stu-id="9fe28-137">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="9fe28-138">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9fe28-138">-Confirm</span></span>
<span data-ttu-id="9fe28-139">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9fe28-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9fe28-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9fe28-140">-WhatIf</span></span>
<span data-ttu-id="9fe28-141">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9fe28-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9fe28-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9fe28-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9fe28-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fe28-143">CommonParameters</span></span>
<span data-ttu-id="9fe28-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9fe28-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fe28-145">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9fe28-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fe28-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9fe28-146">INPUTS</span></span>

### <span data-ttu-id="9fe28-147">System. String</span><span class="sxs-lookup"><span data-stu-id="9fe28-147">System.String</span></span>

### <span data-ttu-id="9fe28-148">System. GUID</span><span class="sxs-lookup"><span data-stu-id="9fe28-148">System.Guid</span></span>

### <span data-ttu-id="9fe28-149">Microsoft. Azure. Command. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="9fe28-149">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="9fe28-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9fe28-150">OUTPUTS</span></span>

### <span data-ttu-id="9fe28-151">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9fe28-151">System.Boolean</span></span>

## <span data-ttu-id="9fe28-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9fe28-152">NOTES</span></span>

## <span data-ttu-id="9fe28-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9fe28-153">RELATED LINKS</span></span>

[<span data-ttu-id="9fe28-154">Get-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="9fe28-154">Get-AzADAppCredential</span></span>](./Get-AzADAppCredential.md)

[<span data-ttu-id="9fe28-155">Új – AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="9fe28-155">New-AzADAppCredential</span></span>](./New-AzADAppCredential.md)

[<span data-ttu-id="9fe28-156">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="9fe28-156">Get-AzADApplication</span></span>](./Get-AzADApplication.md)
