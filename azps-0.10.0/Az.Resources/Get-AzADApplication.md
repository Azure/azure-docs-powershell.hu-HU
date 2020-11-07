---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 66AC5120-80B1-46F2-AA51-132BF361602E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzADApplication.md
ms.openlocfilehash: 5f019f413e7ae0efa2013412499fcf34bd94a248
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843490"
---
# <span data-ttu-id="92e73-101">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="92e73-101">Get-AzADApplication</span></span>

## <span data-ttu-id="92e73-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="92e73-102">SYNOPSIS</span></span>
<span data-ttu-id="92e73-103">Felsorolja a meglévő Azure Active Directory-alkalmazásokat.</span><span class="sxs-lookup"><span data-stu-id="92e73-103">Lists existing azure active directory applications.</span></span>

## <span data-ttu-id="92e73-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="92e73-104">SYNTAX</span></span>

### <span data-ttu-id="92e73-105">EmptyParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="92e73-105">EmptyParameterSet (Default)</span></span>
```
Get-AzADApplication [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="92e73-106">ApplicationObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="92e73-106">ApplicationObjectIdParameterSet</span></span>
```
Get-AzADApplication -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="92e73-107">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="92e73-107">ApplicationIdParameterSet</span></span>
```
Get-AzADApplication -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="92e73-108">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="92e73-108">SearchStringParameterSet</span></span>
```
Get-AzADApplication -DisplayNameStartWith <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="92e73-109">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="92e73-109">DisplayNameParameterSet</span></span>
```
Get-AzADApplication -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="92e73-110">ApplicationIdentifierUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="92e73-110">ApplicationIdentifierUriParameterSet</span></span>
```
Get-AzADApplication -IdentifierUri <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="92e73-111">Leírás</span><span class="sxs-lookup"><span data-stu-id="92e73-111">DESCRIPTION</span></span>
<span data-ttu-id="92e73-112">Felsorolja a meglévő Azure Active Directory-alkalmazásokat.</span><span class="sxs-lookup"><span data-stu-id="92e73-112">Lists existing azure active directory applications.</span></span>
<span data-ttu-id="92e73-113">Az alkalmazások keresése a ObjectId, az ApplicationId, a IdentifierUri vagy a DisplayName segítségével végezhető el.</span><span class="sxs-lookup"><span data-stu-id="92e73-113">Application lookup can be done by ObjectId, ApplicationId, IdentifierUri or DisplayName.</span></span>
<span data-ttu-id="92e73-114">Ha nincs megadva paraméter, a program az összes alkalmazást beolvassa a bérlői webhelyre.</span><span class="sxs-lookup"><span data-stu-id="92e73-114">If no parameter is provided, it fetches all applications under the tenant.</span></span>

## <span data-ttu-id="92e73-115">Példák</span><span class="sxs-lookup"><span data-stu-id="92e73-115">EXAMPLES</span></span>

### <span data-ttu-id="92e73-116">Példa 1 – az összes alkalmazás listázása</span><span class="sxs-lookup"><span data-stu-id="92e73-116">Example 1 - List all applications</span></span>

```
PS C:\> Get-AzADApplication
```

<span data-ttu-id="92e73-117">Felsorolja az összes alkalmazást bérlői fiókban.</span><span class="sxs-lookup"><span data-stu-id="92e73-117">Lists all the applications under a tenant.</span></span>

### <span data-ttu-id="92e73-118">Példa 2 – a lapozást használó alkalmazások listázása</span><span class="sxs-lookup"><span data-stu-id="92e73-118">Example 2 - List applications using paging</span></span>

```
PS C:\> Get-AzADApplication -First 100
```

<span data-ttu-id="92e73-119">Felsorolja az első 100-alkalmazásokat bérlői fiókban.</span><span class="sxs-lookup"><span data-stu-id="92e73-119">Lists the first 100 applications under a tenant.</span></span>

### <span data-ttu-id="92e73-120">Példa: 3 – az alkalmazás beolvasása azonosító URI azonosítóval</span><span class="sxs-lookup"><span data-stu-id="92e73-120">Example 3 - Get application by identifier URI</span></span>

```
PS C:\> Get-AzADApplication -IdentifierUri http://mySecretApp1
```

<span data-ttu-id="92e73-121">A "" azonosítóval kapja meg az alkalmazást http://mySecretApp1 .</span><span class="sxs-lookup"><span data-stu-id="92e73-121">Gets the application with identifier uri as "http://mySecretApp1".</span></span>

### <span data-ttu-id="92e73-122">Példa 4 – alkalmazásobjektum-azonosító beszerzése</span><span class="sxs-lookup"><span data-stu-id="92e73-122">Example 4 - Get application by object id</span></span>

```
PS C:\> Get-AzADApplication -ObjectId 39e64ec6-569b-4030-8e1c-c3c519a05d69
```

<span data-ttu-id="92e73-123">A ' 39e64ec6-569b-4030-8e1c-c3c519a05d69 ' azonosítójú objektummal kapja meg az alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="92e73-123">Gets the application with the object id '39e64ec6-569b-4030-8e1c-c3c519a05d69'.</span></span>

## <span data-ttu-id="92e73-124">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="92e73-124">PARAMETERS</span></span>

### <span data-ttu-id="92e73-125">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="92e73-125">-ApplicationId</span></span>
<span data-ttu-id="92e73-126">A lekérni kívánt alkalmazás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="92e73-126">The application id of the application to fetch.</span></span>

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

### <span data-ttu-id="92e73-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92e73-127">-DefaultProfile</span></span>
<span data-ttu-id="92e73-128">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="92e73-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="92e73-129">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="92e73-129">-DisplayName</span></span>
<span data-ttu-id="92e73-130">Az alkalmazás megjelenítendő neve.</span><span class="sxs-lookup"><span data-stu-id="92e73-130">The display name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: DisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92e73-131">-DisplayNameStartWith</span><span class="sxs-lookup"><span data-stu-id="92e73-131">-DisplayNameStartWith</span></span>
<span data-ttu-id="92e73-132">A megjelenítendő névvel kezdődő összes alkalmazás beolvasása</span><span class="sxs-lookup"><span data-stu-id="92e73-132">Fetch all applications starting with the display name.</span></span>

```yaml
Type: System.String
Parameter Sets: SearchStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92e73-133">– Első</span><span class="sxs-lookup"><span data-stu-id="92e73-133">-First</span></span>
<span data-ttu-id="92e73-134">A visszaadni kívánt objektumok maximális száma.</span><span class="sxs-lookup"><span data-stu-id="92e73-134">The maximum number of objects to return.</span></span>

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92e73-135">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="92e73-135">-IdentifierUri</span></span>
<span data-ttu-id="92e73-136">A beolvasni kívánt alkalmazás egyedi azonosítójának URI azonosítója.</span><span class="sxs-lookup"><span data-stu-id="92e73-136">Unique identifier Uri of the application to fetch.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationIdentifierUriParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92e73-137">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="92e73-137">-IncludeTotalCount</span></span>
<span data-ttu-id="92e73-138">Az adathalmaz objektumainak számát jelzi.</span><span class="sxs-lookup"><span data-stu-id="92e73-138">Reports the number of objects in the data set.</span></span> <span data-ttu-id="92e73-139">Ez a paraméter jelenleg nem tesz semmit.</span><span class="sxs-lookup"><span data-stu-id="92e73-139">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="92e73-140">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="92e73-140">-ObjectId</span></span>
<span data-ttu-id="92e73-141">A beolvasni kívánt alkalmazás objektum-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="92e73-141">The object id of the application to fetch.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92e73-142">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="92e73-142">-Skip</span></span>
<span data-ttu-id="92e73-143">Figyelmen kívül hagyja az első N objektumokat, és a fennmaradó objektumokat kapja.</span><span class="sxs-lookup"><span data-stu-id="92e73-143">Ignores the first N objects and then gets the remaining objects.</span></span>

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92e73-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92e73-144">CommonParameters</span></span>
<span data-ttu-id="92e73-145">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="92e73-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92e73-146">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92e73-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92e73-147">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="92e73-147">INPUTS</span></span>

### <span data-ttu-id="92e73-148">System. GUID</span><span class="sxs-lookup"><span data-stu-id="92e73-148">System.Guid</span></span>

### <span data-ttu-id="92e73-149">System. String</span><span class="sxs-lookup"><span data-stu-id="92e73-149">System.String</span></span>

## <span data-ttu-id="92e73-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="92e73-150">OUTPUTS</span></span>

### <span data-ttu-id="92e73-151">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="92e73-151">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="92e73-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="92e73-152">NOTES</span></span>

## <span data-ttu-id="92e73-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="92e73-153">RELATED LINKS</span></span>

[<span data-ttu-id="92e73-154">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="92e73-154">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

[<span data-ttu-id="92e73-155">Új – AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="92e73-155">New-AzADAppCredential</span></span>](./New-AzADAppCredential.md)

[<span data-ttu-id="92e73-156">Get-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="92e73-156">Get-AzADAppCredential</span></span>](./Get-AzADAppCredential.md)

[<span data-ttu-id="92e73-157">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="92e73-157">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)

[<span data-ttu-id="92e73-158">Set-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="92e73-158">Set-AzADApplication</span></span>](./Set-AzADApplication.md)

[<span data-ttu-id="92e73-159">Új – AzADApplication</span><span class="sxs-lookup"><span data-stu-id="92e73-159">New-AzADApplication</span></span>](./New-AzADApplication.md)

