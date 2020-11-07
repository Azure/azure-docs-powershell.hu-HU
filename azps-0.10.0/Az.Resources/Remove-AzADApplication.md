---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C791C593-F7D5-4961-97F9-E4909813FFE7
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-Azadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzADApplication.md
ms.openlocfilehash: 00c9d6e5a5a729ca5a5119b812873078acb38326
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843290"
---
# <span data-ttu-id="6b036-101">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="6b036-101">Remove-AzADApplication</span></span>

## <span data-ttu-id="6b036-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6b036-102">SYNOPSIS</span></span>
<span data-ttu-id="6b036-103">Törli az Azure Active Directory-alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="6b036-103">Deletes the azure active directory application.</span></span>

## <span data-ttu-id="6b036-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6b036-104">SYNTAX</span></span>

### <span data-ttu-id="6b036-105">ObjectIdParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6b036-105">ObjectIdParameterSet (Default)</span></span>
```
Remove-AzADApplication -ObjectId <Guid> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b036-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6b036-106">ApplicationIdParameterSet</span></span>
```
Remove-AzADApplication -ApplicationId <Guid> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b036-107">ApplicationDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="6b036-107">ApplicationDisplayNameParameterSet</span></span>
```
Remove-AzADApplication -DisplayName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b036-108">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6b036-108">InputObjectParameterSet</span></span>
```
Remove-AzADApplication -InputObject <PSADApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b036-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="6b036-109">DESCRIPTION</span></span>
<span data-ttu-id="6b036-110">Törli az Azure Active Directory-alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="6b036-110">Deletes the azure active directory application.</span></span>

## <span data-ttu-id="6b036-111">Példák</span><span class="sxs-lookup"><span data-stu-id="6b036-111">EXAMPLES</span></span>

### <span data-ttu-id="6b036-112">Példa 1 – az alkalmazás objektum-azonosítóval való eltávolítása</span><span class="sxs-lookup"><span data-stu-id="6b036-112">Example 1 - Remove application by object id</span></span>

```
PS C:\> Remove-AzADApplication -ObjectId b4cd1619-80b3-4cfb-9f8f-9f2333425738
```

<span data-ttu-id="6b036-113">Eltávolítja az "b4cd1619-80b3-4cfb-9f8f-9f2333425738" azonosítójú alkalmazást a bérlői webhelyről.</span><span class="sxs-lookup"><span data-stu-id="6b036-113">Removes the application with object id 'b4cd1619-80b3-4cfb-9f8f-9f2333425738' from the tenant.</span></span>

### <span data-ttu-id="6b036-114">Példa 2 – alkalmazás-azonosító eltávolítása</span><span class="sxs-lookup"><span data-stu-id="6b036-114">Example 2 - Remove application by application id</span></span>

```
PS C:\> Remove-AzADApplication -ApplicationId f9c5ea4f-28f0-401a-a491-491a037fa346
```

<span data-ttu-id="6b036-115">Eltávolítja az "f9c5ea4f-28f0-401a-a491-491a037fa346" azonosítójú alkalmazást a bérlői webhelyről.</span><span class="sxs-lookup"><span data-stu-id="6b036-115">Removes the application with application id 'f9c5ea4f-28f0-401a-a491-491a037fa346' from the tenant.</span></span>

### <span data-ttu-id="6b036-116">3 példa – alkalmazás eltávolítása csővezetékről</span><span class="sxs-lookup"><span data-stu-id="6b036-116">Example 3 - Remove application by piping</span></span>

```
PS C:\> Get-AzADApplication -ObjectId b4cd1619-80b3-4cfb-9f8f-9f2333425738 | Remove-AzADApplication
```

<span data-ttu-id="6b036-117">Beolvassa az alkalmazást a "b4cd1619-80b3-4cfb-9f8f-9f2333425738" azonosítójú azonosítójú objektummal, és a Remove-AzADApplication parancsmaghoz tartozó csövekkel eltávolíthatja az alkalmazást a bérlői webhelyről.</span><span class="sxs-lookup"><span data-stu-id="6b036-117">Gets the application with object id 'b4cd1619-80b3-4cfb-9f8f-9f2333425738' and pipes that to the Remove-AzADApplication cmdlet to remove the application from the tenant.</span></span>

## <span data-ttu-id="6b036-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6b036-118">PARAMETERS</span></span>

### <span data-ttu-id="6b036-119">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="6b036-119">-ApplicationId</span></span>
<span data-ttu-id="6b036-120">Az eltávolítandó alkalmazás alkalmazás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="6b036-120">The application id of the application to remove.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b036-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b036-121">-DefaultProfile</span></span>
<span data-ttu-id="6b036-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="6b036-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6b036-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="6b036-123">-DisplayName</span></span>
<span data-ttu-id="6b036-124">Az alkalmazás megjelenítendő neve.</span><span class="sxs-lookup"><span data-stu-id="6b036-124">The display name of the application.</span></span>

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

### <span data-ttu-id="6b036-125">-Force</span><span class="sxs-lookup"><span data-stu-id="6b036-125">-Force</span></span>
<span data-ttu-id="6b036-126">Ha megerősítés nélkül szeretne törölni egy alkalmazást, váltson.</span><span class="sxs-lookup"><span data-stu-id="6b036-126">Switch to delete an application without a confirmation.</span></span>

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

### <span data-ttu-id="6b036-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6b036-127">-InputObject</span></span>
<span data-ttu-id="6b036-128">Az eltávolítandó alkalmazást jelző objektum.</span><span class="sxs-lookup"><span data-stu-id="6b036-128">The object representing the application to remove.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6b036-129">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="6b036-129">-ObjectId</span></span>
<span data-ttu-id="6b036-130">A törlendő alkalmazás objektum-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="6b036-130">The object id of the application to delete.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b036-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6b036-131">-PassThru</span></span>
<span data-ttu-id="6b036-132">Ez a beállítás akkor igaz, ha a parancs sikeres.</span><span class="sxs-lookup"><span data-stu-id="6b036-132">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="6b036-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6b036-133">-Confirm</span></span>
<span data-ttu-id="6b036-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6b036-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b036-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b036-135">-WhatIf</span></span>
<span data-ttu-id="6b036-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6b036-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b036-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6b036-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b036-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b036-138">CommonParameters</span></span>
<span data-ttu-id="6b036-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6b036-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b036-140">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b036-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b036-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6b036-141">INPUTS</span></span>

### <span data-ttu-id="6b036-142">System. GUID</span><span class="sxs-lookup"><span data-stu-id="6b036-142">System.Guid</span></span>

### <span data-ttu-id="6b036-143">System. String</span><span class="sxs-lookup"><span data-stu-id="6b036-143">System.String</span></span>

### <span data-ttu-id="6b036-144">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="6b036-144">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>
<span data-ttu-id="6b036-145">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="6b036-145">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="6b036-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6b036-146">OUTPUTS</span></span>

### <span data-ttu-id="6b036-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6b036-147">System.Boolean</span></span>

## <span data-ttu-id="6b036-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6b036-148">NOTES</span></span>
<span data-ttu-id="6b036-149">Kulcsszavak: Azure, az, kar, erőforrás, kezelés, vezető, erőforrás, csoport, sablon, központi telepítő</span><span class="sxs-lookup"><span data-stu-id="6b036-149">Keywords: azure, Az, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="6b036-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6b036-150">RELATED LINKS</span></span>

[<span data-ttu-id="6b036-151">Új – AzADApplication</span><span class="sxs-lookup"><span data-stu-id="6b036-151">New-AzADApplication</span></span>](./New-AzADApplication.md)

[<span data-ttu-id="6b036-152">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="6b036-152">Get-AzADApplication</span></span>](./Get-AzADApplication.md)

[<span data-ttu-id="6b036-153">Set-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="6b036-153">Set-AzADApplication</span></span>](./Set-AzADApplication.md)

[<span data-ttu-id="6b036-154">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="6b036-154">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

