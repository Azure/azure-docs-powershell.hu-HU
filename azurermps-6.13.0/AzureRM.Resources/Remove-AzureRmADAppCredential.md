---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C61FA834-BEBE-4DBF-888F-C6CB8CC95390
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermadappcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADAppCredential.md
ms.openlocfilehash: 6c076258acd19714f30976fd353d7cbbacdf1d94
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493945"
---
# <span data-ttu-id="500a2-101">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="500a2-101">Remove-AzureRmADAppCredential</span></span>

## <span data-ttu-id="500a2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="500a2-102">SYNOPSIS</span></span>
<span data-ttu-id="500a2-103">Hitelesítő adatok eltávolítása egy alkalmazásból.</span><span class="sxs-lookup"><span data-stu-id="500a2-103">Removes a credential from an application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="500a2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="500a2-104">SYNTAX</span></span>

### <span data-ttu-id="500a2-105">ApplicationObjectIdWithKeyIdParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="500a2-105">ApplicationObjectIdWithKeyIdParameterSet (Default)</span></span>
```
Remove-AzureRmADAppCredential -ObjectId <Guid> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="500a2-106">ApplicationIdWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="500a2-106">ApplicationIdWithKeyIdParameterSet</span></span>
```
Remove-AzureRmADAppCredential -ApplicationId <Guid> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="500a2-107">ApplicationDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="500a2-107">ApplicationDisplayNameParameterSet</span></span>
```
Remove-AzureRmADAppCredential -DisplayName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="500a2-108">ApplicationObjectWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="500a2-108">ApplicationObjectWithKeyIdParameterSet</span></span>
```
Remove-AzureRmADAppCredential [-KeyId <Guid>] -ApplicationObject <PSADApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="500a2-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="500a2-109">DESCRIPTION</span></span>
<span data-ttu-id="500a2-110">A Remove-AzureRmADAppCredential parancsmagot kiegyezéssel vagy a hitelesítő adatok kulcsának lejárati időpontjának részeként lehet eltávolítani egy alkalmazás hitelesítő kulcsával.</span><span class="sxs-lookup"><span data-stu-id="500a2-110">The Remove-AzureRmADAppCredential cmdlet can be used to remove a credential key from an application in the case of a compromise or as part of credential key rollover expiration.</span></span>
<span data-ttu-id="500a2-111">Az alkalmazás azonosítása az objektum-azonosító vagy a AppId megadásával történik.</span><span class="sxs-lookup"><span data-stu-id="500a2-111">The application is identified by supplying either the object ID or AppId.</span></span>
<span data-ttu-id="500a2-112">Az eltávolítandó hitelesítő adatok azonosítása a kulcs azonosítója alapján történik.</span><span class="sxs-lookup"><span data-stu-id="500a2-112">The credential to be removed is identified by its key ID.</span></span>

## <span data-ttu-id="500a2-113">Példák</span><span class="sxs-lookup"><span data-stu-id="500a2-113">EXAMPLES</span></span>

### <span data-ttu-id="500a2-114">Példa 1 – meghatározott hitelesítő adatok eltávolítása egy alkalmazásból</span><span class="sxs-lookup"><span data-stu-id="500a2-114">Example 1 - Remove a specific credential from an application</span></span>

```
PS C:\> Remove-AzureRmADAppCredential -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 -KeyId 9044423a-60a3-45ac-9ab1-09534157ebb
```

<span data-ttu-id="500a2-115">Eltávolítja a "9044423a-60a3-45ac-9ab1-09534157ebb" azonosítójú hitelesítő adatokat a "7663d3fb-6f86-4352-9e6d-cf9d50d5ee82" azonosítójú alkalmazásból.</span><span class="sxs-lookup"><span data-stu-id="500a2-115">Removes the credential with key id '9044423a-60a3-45ac-9ab1-09534157ebb' from the application with object id '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82'.</span></span>

### <span data-ttu-id="500a2-116">2. példa – az összes hitelesítő adat eltávolítása egy alkalmazásból</span><span class="sxs-lookup"><span data-stu-id="500a2-116">Example 2 - Remove all credentials from an application</span></span>

```
PS C:\> Remove-AzureRmADAppCredential -ApplicationId 4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58
```

<span data-ttu-id="500a2-117">A "4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58" azonosítójú alkalmazásban az összes hitelesítő adat eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="500a2-117">Removes all credentials from the application with application id '4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58'.</span></span>

### <span data-ttu-id="500a2-118">3 példa – az összes hitelesítő adat eltávolítása a csővezetékekkel</span><span class="sxs-lookup"><span data-stu-id="500a2-118">Example 3 - Remove all credentials using piping</span></span>

```
PS C:\> Get-AzureRmADApplication -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 | Remove-AzureRmADAppCredential
```

<span data-ttu-id="500a2-119">Beilleszti az alkalmazást a "7663d3fb-6f86-4352-9e6d-cf9d50d5ee82" azonosítójú objektumazonosítót, valamint az Remove-AzureRmADAppCredential parancsmaghoz tartozó csöveket, és eltávolítja az adott alkalmazás összes hitelesítő adatait.</span><span class="sxs-lookup"><span data-stu-id="500a2-119">Gets the application with object id '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82' and pipes that to the Remove-AzureRmADAppCredential cmdlet and removes all credentials from that application.</span></span>

## <span data-ttu-id="500a2-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="500a2-120">PARAMETERS</span></span>

### <span data-ttu-id="500a2-121">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="500a2-121">-ApplicationId</span></span>
<span data-ttu-id="500a2-122">Az alkalmazás azonosítója a hitelesítő adatok eltávolításához.</span><span class="sxs-lookup"><span data-stu-id="500a2-122">The id of the application to remove the credentials from.</span></span>

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

### <span data-ttu-id="500a2-123">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="500a2-123">-ApplicationObject</span></span>
<span data-ttu-id="500a2-124">Az Application objektum a hitelesítő adatok eltávolításához.</span><span class="sxs-lookup"><span data-stu-id="500a2-124">The application object to remove the credentials from.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="500a2-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="500a2-125">-DefaultProfile</span></span>
<span data-ttu-id="500a2-126">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="500a2-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="500a2-127">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="500a2-127">-DisplayName</span></span>
<span data-ttu-id="500a2-128">Az alkalmazás megjelenítendő neve.</span><span class="sxs-lookup"><span data-stu-id="500a2-128">The display name of the application.</span></span>

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

### <span data-ttu-id="500a2-129">-Force</span><span class="sxs-lookup"><span data-stu-id="500a2-129">-Force</span></span>
<span data-ttu-id="500a2-130">Váltás a hitelesítő adatok törlésére megerősítés nélkül.</span><span class="sxs-lookup"><span data-stu-id="500a2-130">Switch to delete credential without a confirmation.</span></span>

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

### <span data-ttu-id="500a2-131">-KeyId</span><span class="sxs-lookup"><span data-stu-id="500a2-131">-KeyId</span></span>
<span data-ttu-id="500a2-132">Az eltávolítandó hitelesítőadat-kulcsot adja meg.</span><span class="sxs-lookup"><span data-stu-id="500a2-132">Specifies the credential key to be removed.</span></span>
<span data-ttu-id="500a2-133">Az alkalmazáshoz tartozó kulcs-azonosítók az Get-AzureRmADAppCredential parancsmag használatával szerezhetők be.</span><span class="sxs-lookup"><span data-stu-id="500a2-133">The key Ids for the application can be obtained using the Get-AzureRmADAppCredential cmdlet.</span></span>

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

### <span data-ttu-id="500a2-134">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="500a2-134">-ObjectId</span></span>
<span data-ttu-id="500a2-135">Az alkalmazás Object ID-je a hitelesítő adatok eltávolításához.</span><span class="sxs-lookup"><span data-stu-id="500a2-135">The object id of the application to remove the credentials from.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationObjectIdWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="500a2-136">-PassThru</span><span class="sxs-lookup"><span data-stu-id="500a2-136">-PassThru</span></span>
<span data-ttu-id="500a2-137">Ez a beállítás akkor igaz, ha a parancs sikeres.</span><span class="sxs-lookup"><span data-stu-id="500a2-137">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="500a2-138">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="500a2-138">-Confirm</span></span>
<span data-ttu-id="500a2-139">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="500a2-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="500a2-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="500a2-140">-WhatIf</span></span>
<span data-ttu-id="500a2-141">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="500a2-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="500a2-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="500a2-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="500a2-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="500a2-143">CommonParameters</span></span>
<span data-ttu-id="500a2-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="500a2-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="500a2-145">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="500a2-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="500a2-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="500a2-146">INPUTS</span></span>

### <span data-ttu-id="500a2-147">System. GUID</span><span class="sxs-lookup"><span data-stu-id="500a2-147">System.Guid</span></span>

### <span data-ttu-id="500a2-148">System. String</span><span class="sxs-lookup"><span data-stu-id="500a2-148">System.String</span></span>

### <span data-ttu-id="500a2-149">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="500a2-149">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>
<span data-ttu-id="500a2-150">Paraméterek: ApplicationObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="500a2-150">Parameters: ApplicationObject (ByValue)</span></span>

## <span data-ttu-id="500a2-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="500a2-151">OUTPUTS</span></span>

### <span data-ttu-id="500a2-152">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="500a2-152">System.Boolean</span></span>

## <span data-ttu-id="500a2-153">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="500a2-153">NOTES</span></span>

## <span data-ttu-id="500a2-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="500a2-154">RELATED LINKS</span></span>

[<span data-ttu-id="500a2-155">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="500a2-155">Get-AzureRmADAppCredential</span></span>](./Get-AzureRmADAppCredential.md)

[<span data-ttu-id="500a2-156">Új – AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="500a2-156">New-AzureRmADAppCredential</span></span>](./New-AzureRmADAppCredential.md)

[<span data-ttu-id="500a2-157">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="500a2-157">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)
