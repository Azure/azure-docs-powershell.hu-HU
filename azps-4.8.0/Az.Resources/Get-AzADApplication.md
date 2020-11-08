---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 66AC5120-80B1-46F2-AA51-132BF361602E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADApplication.md
ms.openlocfilehash: 68344fcafa16187651615c95ec2fb41d0bbbfb82
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182172"
---
# <span data-ttu-id="b66c3-101">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="b66c3-101">Get-AzADApplication</span></span>

## <span data-ttu-id="b66c3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b66c3-102">SYNOPSIS</span></span>
<span data-ttu-id="b66c3-103">Felsorolja a meglévő Azure Active Directory-alkalmazásokat.</span><span class="sxs-lookup"><span data-stu-id="b66c3-103">Lists existing azure active directory applications.</span></span>

## <span data-ttu-id="b66c3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b66c3-104">SYNTAX</span></span>

### <span data-ttu-id="b66c3-105">EmptyParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b66c3-105">EmptyParameterSet (Default)</span></span>
```
Get-AzADApplication [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="b66c3-106">ApplicationObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b66c3-106">ApplicationObjectIdParameterSet</span></span>
```
Get-AzADApplication -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="b66c3-107">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b66c3-107">ApplicationIdParameterSet</span></span>
```
Get-AzADApplication -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="b66c3-108">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="b66c3-108">SearchStringParameterSet</span></span>
```
Get-AzADApplication -DisplayNameStartWith <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="b66c3-109">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b66c3-109">DisplayNameParameterSet</span></span>
```
Get-AzADApplication -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="b66c3-110">ApplicationIdentifierUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="b66c3-110">ApplicationIdentifierUriParameterSet</span></span>
```
Get-AzADApplication -IdentifierUri <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="b66c3-111">Leírás</span><span class="sxs-lookup"><span data-stu-id="b66c3-111">DESCRIPTION</span></span>
<span data-ttu-id="b66c3-112">Felsorolja a meglévő Azure Active Directory-alkalmazásokat.</span><span class="sxs-lookup"><span data-stu-id="b66c3-112">Lists existing azure active directory applications.</span></span>
<span data-ttu-id="b66c3-113">Az alkalmazások keresése a ObjectId, az ApplicationId, a IdentifierUri vagy a DisplayName segítségével végezhető el.</span><span class="sxs-lookup"><span data-stu-id="b66c3-113">Application lookup can be done by ObjectId, ApplicationId, IdentifierUri or DisplayName.</span></span>
<span data-ttu-id="b66c3-114">Ha nincs megadva paraméter, a program az összes alkalmazást beolvassa a bérlői webhelyre.</span><span class="sxs-lookup"><span data-stu-id="b66c3-114">If no parameter is provided, it fetches all applications under the tenant.</span></span>

## <span data-ttu-id="b66c3-115">Példák</span><span class="sxs-lookup"><span data-stu-id="b66c3-115">EXAMPLES</span></span>

### <span data-ttu-id="b66c3-116">Példa 1 – az összes alkalmazás listázása</span><span class="sxs-lookup"><span data-stu-id="b66c3-116">Example 1 - List all applications</span></span>

```
PS C:\> Get-AzADApplication
```

<span data-ttu-id="b66c3-117">Felsorolja az összes alkalmazást bérlői fiókban.</span><span class="sxs-lookup"><span data-stu-id="b66c3-117">Lists all the applications under a tenant.</span></span>

### <span data-ttu-id="b66c3-118">Példa 2 – a lapozást használó alkalmazások listázása</span><span class="sxs-lookup"><span data-stu-id="b66c3-118">Example 2 - List applications using paging</span></span>

```
PS C:\> Get-AzADApplication -First 100
```

<span data-ttu-id="b66c3-119">Felsorolja az első 100-alkalmazásokat bérlői fiókban.</span><span class="sxs-lookup"><span data-stu-id="b66c3-119">Lists the first 100 applications under a tenant.</span></span>

### <span data-ttu-id="b66c3-120">Példa: 3 – az alkalmazás beolvasása azonosító URI azonosítóval</span><span class="sxs-lookup"><span data-stu-id="b66c3-120">Example 3 - Get application by identifier URI</span></span>

```
PS C:\> Get-AzADApplication -IdentifierUri http://mySecretApp1
```

<span data-ttu-id="b66c3-121">A "" azonosítóval kapja meg az alkalmazást http://mySecretApp1 .</span><span class="sxs-lookup"><span data-stu-id="b66c3-121">Gets the application with identifier uri as "http://mySecretApp1".</span></span>

### <span data-ttu-id="b66c3-122">Példa 4 – alkalmazásobjektum-azonosító beszerzése</span><span class="sxs-lookup"><span data-stu-id="b66c3-122">Example 4 - Get application by object id</span></span>

```
PS C:\> Get-AzADApplication -ObjectId 39e64ec6-569b-4030-8e1c-c3c519a05d69
```

<span data-ttu-id="b66c3-123">A ' 39e64ec6-569b-4030-8e1c-c3c519a05d69 ' azonosítójú objektummal kapja meg az alkalmazást.</span><span class="sxs-lookup"><span data-stu-id="b66c3-123">Gets the application with the object id '39e64ec6-569b-4030-8e1c-c3c519a05d69'.</span></span>

## <span data-ttu-id="b66c3-124">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b66c3-124">PARAMETERS</span></span>

### <span data-ttu-id="b66c3-125">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="b66c3-125">-ApplicationId</span></span>
<span data-ttu-id="b66c3-126">A lekérni kívánt alkalmazás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="b66c3-126">The application id of the application to fetch.</span></span>

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

### <span data-ttu-id="b66c3-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b66c3-127">-DefaultProfile</span></span>
<span data-ttu-id="b66c3-128">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="b66c3-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b66c3-129">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="b66c3-129">-DisplayName</span></span>
<span data-ttu-id="b66c3-130">Az alkalmazás megjelenítendő neve.</span><span class="sxs-lookup"><span data-stu-id="b66c3-130">The display name of the application.</span></span>

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

### <span data-ttu-id="b66c3-131">-DisplayNameStartWith</span><span class="sxs-lookup"><span data-stu-id="b66c3-131">-DisplayNameStartWith</span></span>
<span data-ttu-id="b66c3-132">A megjelenítendő névvel kezdődő összes alkalmazás beolvasása</span><span class="sxs-lookup"><span data-stu-id="b66c3-132">Fetch all applications starting with the display name.</span></span>

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

### <span data-ttu-id="b66c3-133">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="b66c3-133">-IdentifierUri</span></span>
<span data-ttu-id="b66c3-134">A beolvasni kívánt alkalmazás egyedi azonosítójának URI azonosítója.</span><span class="sxs-lookup"><span data-stu-id="b66c3-134">Unique identifier Uri of the application to fetch.</span></span>

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

### <span data-ttu-id="b66c3-135">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="b66c3-135">-ObjectId</span></span>
<span data-ttu-id="b66c3-136">A beolvasni kívánt alkalmazás objektum-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="b66c3-136">The object id of the application to fetch.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b66c3-137">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="b66c3-137">-IncludeTotalCount</span></span>
<span data-ttu-id="b66c3-138">Az adathalmaz objektumainak számát jelzi.</span><span class="sxs-lookup"><span data-stu-id="b66c3-138">Reports the number of objects in the data set.</span></span> <span data-ttu-id="b66c3-139">Ez a paraméter jelenleg nem tesz semmit.</span><span class="sxs-lookup"><span data-stu-id="b66c3-139">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="b66c3-140">-Skip (kihagyás)</span><span class="sxs-lookup"><span data-stu-id="b66c3-140">-Skip</span></span>
<span data-ttu-id="b66c3-141">Figyelmen kívül hagyja az első N objektumokat, és a fennmaradó objektumokat kapja.</span><span class="sxs-lookup"><span data-stu-id="b66c3-141">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="b66c3-142">– Első</span><span class="sxs-lookup"><span data-stu-id="b66c3-142">-First</span></span>
<span data-ttu-id="b66c3-143">A visszaadni kívánt objektumok maximális száma.</span><span class="sxs-lookup"><span data-stu-id="b66c3-143">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="b66c3-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b66c3-144">CommonParameters</span></span>
<span data-ttu-id="b66c3-145">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b66c3-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b66c3-146">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b66c3-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b66c3-147">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b66c3-147">INPUTS</span></span>

### <span data-ttu-id="b66c3-148">System. String</span><span class="sxs-lookup"><span data-stu-id="b66c3-148">System.String</span></span>

### <span data-ttu-id="b66c3-149">System. GUID</span><span class="sxs-lookup"><span data-stu-id="b66c3-149">System.Guid</span></span>

## <span data-ttu-id="b66c3-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b66c3-150">OUTPUTS</span></span>

### <span data-ttu-id="b66c3-151">Microsoft. Azure. Command. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="b66c3-151">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="b66c3-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b66c3-152">NOTES</span></span>

## <span data-ttu-id="b66c3-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b66c3-153">RELATED LINKS</span></span>

[<span data-ttu-id="b66c3-154">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="b66c3-154">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

[<span data-ttu-id="b66c3-155">Új – AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="b66c3-155">New-AzADAppCredential</span></span>](./New-AzADAppCredential.md)

[<span data-ttu-id="b66c3-156">Get-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="b66c3-156">Get-AzADAppCredential</span></span>](./Get-AzADAppCredential.md)

[<span data-ttu-id="b66c3-157">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="b66c3-157">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)

[<span data-ttu-id="b66c3-158">Új – AzADApplication</span><span class="sxs-lookup"><span data-stu-id="b66c3-158">New-AzADApplication</span></span>](./New-AzADApplication.md)

[<span data-ttu-id="b66c3-159">Update-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="b66c3-159">Update-AzADApplication</span></span>](./Update-AzADApplication.md)

