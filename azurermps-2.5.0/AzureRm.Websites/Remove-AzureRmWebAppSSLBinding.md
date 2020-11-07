---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 3AB3D398-E5DB-4214-BA27-6E3B7D225550
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/remove-azurermwebappsslbinding
schema: 2.0.0
ms.openlocfilehash: 06bb13207a666b4537c267e391818865e4165e74
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848053"
---
# <span data-ttu-id="2a4fd-101">Remove-AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="2a4fd-101">Remove-AzureRmWebAppSSLBinding</span></span>

## <span data-ttu-id="2a4fd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2a4fd-102">SYNOPSIS</span></span>
<span data-ttu-id="2a4fd-103">SSL-kötés eltávolítása feltöltött tanúsítványból.</span><span class="sxs-lookup"><span data-stu-id="2a4fd-103">Removes an SSL binding from an uploaded certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2a4fd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2a4fd-104">SYNTAX</span></span>

### <span data-ttu-id="2a4fd-105">S1</span><span class="sxs-lookup"><span data-stu-id="2a4fd-105">S1</span></span>
```
Remove-AzureRmWebAppSSLBinding [-Name] <String> [[-DeleteCertificate] <Boolean>] [-Force]
 [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a4fd-106">S2</span><span class="sxs-lookup"><span data-stu-id="2a4fd-106">S2</span></span>
```
Remove-AzureRmWebAppSSLBinding [-Name] <String> [[-DeleteCertificate] <Boolean>] [-Force] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a4fd-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="2a4fd-107">DESCRIPTION</span></span>
<span data-ttu-id="2a4fd-108">A **Remove-AzureRmWebAppSSLBinding** parancsmag egy biztonságos szoftvercsatorna-RÉTEGET (SSL-kötést) távolít el az Azure Web App alkalmazásból.</span><span class="sxs-lookup"><span data-stu-id="2a4fd-108">The **Remove-AzureRmWebAppSSLBinding** cmdlet removes a Secure Sockets Layer (SSL) binding from an Azure Web App.</span></span>
<span data-ttu-id="2a4fd-109">Az SSL-kötések segítségével webalkalmazásokat társíthat egy tanúsítványhoz.</span><span class="sxs-lookup"><span data-stu-id="2a4fd-109">SSL bindings are used to associate a Web App with a certificate.</span></span>

## <span data-ttu-id="2a4fd-110">Példák</span><span class="sxs-lookup"><span data-stu-id="2a4fd-110">EXAMPLES</span></span>

### <span data-ttu-id="2a4fd-111">1. példa: egy webalkalmazás SSL-kötésének eltávolítása</span><span class="sxs-lookup"><span data-stu-id="2a4fd-111">Example 1: Remove an SSL binding for a web app</span></span>
```
PS C:\>Remove-AzureRmWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Name "www.contoso.com"
```

<span data-ttu-id="2a4fd-112">Ez a parancs eltávolítja a Web App ContosoWebApp tartozó SSL-kötést.</span><span class="sxs-lookup"><span data-stu-id="2a4fd-112">This command removes the SSL binding for the web app ContosoWebApp.</span></span>
<span data-ttu-id="2a4fd-113">Mivel a *DeleteCertificate* paraméter nem szerepel a listában, a rendszer törli a tanúsítványt, ha már nincs SSL-kötése.</span><span class="sxs-lookup"><span data-stu-id="2a4fd-113">Since the *DeleteCertificate* parameter is not included, the certificate will be deleted if it no longer has any SSL bindings.</span></span>

### <span data-ttu-id="2a4fd-114">2. példa: SSL-kötés eltávolítása a tanúsítvány eltávolítása nélkül</span><span class="sxs-lookup"><span data-stu-id="2a4fd-114">Example 2: Remove an SSL binding without removing the certificate</span></span>
```
PS C:\>Remove-AzureRmWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Name "www.contoso.com" -DeleteCertificate $False
```

<span data-ttu-id="2a4fd-115">Az 1 értékhez hasonlóan a parancs eltávolítja az SSL-kötést a Web App ContosoWebApp.</span><span class="sxs-lookup"><span data-stu-id="2a4fd-115">Similar to Example 1, this command also removes the SSL binding for the Web App ContosoWebApp.</span></span>
<span data-ttu-id="2a4fd-116">Ebben az esetben azonban a *DeleteCertificate* paraméter szerepel, és a paraméter értéke $false értékre van állítva.</span><span class="sxs-lookup"><span data-stu-id="2a4fd-116">In this case, however, the *DeleteCertificate* parameter is included, and the parameter value is set to $False.</span></span>
<span data-ttu-id="2a4fd-117">Ez azt jelenti, hogy a tanúsítvány nem törlődik, függetlenül attól, hogy SSL-kötést tartalmaz-e vagy sem.</span><span class="sxs-lookup"><span data-stu-id="2a4fd-117">That means that the certificate will not be deleted regardless of whether it has any SSL bindings or not.</span></span>

### <span data-ttu-id="2a4fd-118">3. példa: egy objektum-hivatkozás használatával eltávolíthatja az SSL-kötést</span><span class="sxs-lookup"><span data-stu-id="2a4fd-118">Example 3: Use an object reference to remove an SSL binding</span></span>
```
PS C:\>$WebApp = Get-AzureRmWebApp -Name "ContosoWebApp"
PS C:\> Remove-AzureRmWebAppSSLBinding -WebApp $WebApp -Name "www.contoso.com"
```

<span data-ttu-id="2a4fd-119">Ez a példa egy objektum hivatkozását használja a webalkalmazás webhelyére a webalkalmazások SSL-kötésének eltávolításához.</span><span class="sxs-lookup"><span data-stu-id="2a4fd-119">This example uses an object reference to the Web App website to remove the SSL binding for a Web App.</span></span>

<span data-ttu-id="2a4fd-120">Az első parancs az Get-AzureRmWebApp parancsmagot használja a ContosoWebApp nevű webalkalmazás objektum-hivatkozásának létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="2a4fd-120">The first command uses the Get-AzureRmWebApp cmdlet to create an object reference to the Web App named ContosoWebApp.</span></span>
<span data-ttu-id="2a4fd-121">Az objektum hivatkozása $WebApp nevű változóban tárolódik.</span><span class="sxs-lookup"><span data-stu-id="2a4fd-121">That object reference is stored in a variable named $WebApp.</span></span>

<span data-ttu-id="2a4fd-122">A második parancs az Object Reference és az **Remove-AzureRmWebAppSSLBinding** parancsmagot használja az SSL-kötés eltávolításához.</span><span class="sxs-lookup"><span data-stu-id="2a4fd-122">The second command uses the object reference and the **Remove-AzureRmWebAppSSLBinding** cmdlet to remove the SSL binding.</span></span>

## <span data-ttu-id="2a4fd-123">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2a4fd-123">PARAMETERS</span></span>

### <span data-ttu-id="2a4fd-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a4fd-124">-DefaultProfile</span></span>
<span data-ttu-id="2a4fd-125">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2a4fd-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a4fd-126">-DeleteCertificate</span><span class="sxs-lookup"><span data-stu-id="2a4fd-126">-DeleteCertificate</span></span>
<span data-ttu-id="2a4fd-127">Azt a műveletsort adja meg, amelyet akkor kell végrehajtani, ha az SSL-kötés megszűnt a tanúsítvány által használt egyetlen kötés.</span><span class="sxs-lookup"><span data-stu-id="2a4fd-127">Specifies the action to take place if the SSL binding being removed is the only binding used by the certificate.</span></span>
<span data-ttu-id="2a4fd-128">Ha a *DeleteCertificate* értéke $false, a program nem törli a tanúsítványt a kötés törlésekor.</span><span class="sxs-lookup"><span data-stu-id="2a4fd-128">If *DeleteCertificate* is set to $False, the certificate will not be deleted when the binding is deleted.</span></span>
<span data-ttu-id="2a4fd-129">Ha a *DeleteCertificate* értéke $TRUE vagy nem szerepel a parancsban, a tanúsítványt az SSL-kötéssel együtt törli a rendszer.</span><span class="sxs-lookup"><span data-stu-id="2a4fd-129">If *DeleteCertificate* is set to $True or is not included in the command, the certificate will be deleted along with the SSL binding.</span></span>

<span data-ttu-id="2a4fd-130">A tanúsítvány csak akkor törlődik, ha az SSL-kötés megszűnt a tanúsítvány által használt egyetlen kötés.</span><span class="sxs-lookup"><span data-stu-id="2a4fd-130">The certificate will only be deleted if the SSL binding being removed is the only binding used by the certificate.</span></span>
<span data-ttu-id="2a4fd-131">Ha a tanúsítvány több kötéssel rendelkezik, akkor a tanúsítvány nem törlődik, függetlenül a *DeleteCertificate* paraméter értékétől.</span><span class="sxs-lookup"><span data-stu-id="2a4fd-131">If the certificate has more than one binding, the certificate will not be removed regardless of the value of the *DeleteCertificate* parameter.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a4fd-132">-Force</span><span class="sxs-lookup"><span data-stu-id="2a4fd-132">-Force</span></span>
<span data-ttu-id="2a4fd-133">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="2a4fd-133">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a4fd-134">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2a4fd-134">-Name</span></span>
<span data-ttu-id="2a4fd-135">A webalkalmazás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2a4fd-135">Specifies the name of the Web App.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a4fd-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a4fd-136">-ResourceGroupName</span></span>
<span data-ttu-id="2a4fd-137">Annak az erőforráscsoportnek a neve, amelyhez a tanúsítvány van rendelve.</span><span class="sxs-lookup"><span data-stu-id="2a4fd-137">Specifies the name of the resource group that the certificate is assigned to.</span></span>

<span data-ttu-id="2a4fd-138">A *ResourceGroupName* paraméter és a *WebApp* paraméter nem használható ugyanabban a parancsban.</span><span class="sxs-lookup"><span data-stu-id="2a4fd-138">You cannot use the *ResourceGroupName* parameter and the *WebApp* parameter in the same command.</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a4fd-139">-Slot</span><span class="sxs-lookup"><span data-stu-id="2a4fd-139">-Slot</span></span>
<span data-ttu-id="2a4fd-140">A Web App telepítő bővítőhelyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2a4fd-140">Specifies the Web App deployment slot.</span></span>
<span data-ttu-id="2a4fd-141">Ha egy központi telepítő bővítőhelyet szeretne használni, használja az Get-AzureRMWebAppSlot parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="2a4fd-141">To get a deployment slot, use the Get-AzureRMWebAppSlot cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a4fd-142">-WebApp</span><span class="sxs-lookup"><span data-stu-id="2a4fd-142">-WebApp</span></span>
<span data-ttu-id="2a4fd-143">Egy webalkalmazást ad meg.</span><span class="sxs-lookup"><span data-stu-id="2a4fd-143">Specifies a Web App.</span></span>
<span data-ttu-id="2a4fd-144">Ha egy webalkalmazást szeretne beszerezni, használja az Get-AzureRmWebApp parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="2a4fd-144">To get a Web App, use the Get-AzureRmWebApp cmdlet.</span></span>

<span data-ttu-id="2a4fd-145">A *WebApp* paraméter nem használható ugyanabban a parancsban, mint a *ResourceGroupName* paraméter és/vagy a *WebAppName*.</span><span class="sxs-lookup"><span data-stu-id="2a4fd-145">You cannot use the *WebApp* parameter in the same command as the *ResourceGroupName* parameter and/or the *WebAppName*.</span></span>

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2a4fd-146">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="2a4fd-146">-WebAppName</span></span>
<span data-ttu-id="2a4fd-147">A webalkalmazás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2a4fd-147">Specifies the name of the Web App.</span></span>

<span data-ttu-id="2a4fd-148">A *WebAppName* paraméter és a *WebApp* paraméter nem használható ugyanabban a parancsban.</span><span class="sxs-lookup"><span data-stu-id="2a4fd-148">You cannot use the *WebAppName* parameter and the *WebApp* parameter in the same command.</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a4fd-149">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2a4fd-149">-Confirm</span></span>
<span data-ttu-id="2a4fd-150">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2a4fd-150">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a4fd-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a4fd-151">-WhatIf</span></span>
<span data-ttu-id="2a4fd-152">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2a4fd-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a4fd-153">A parancsmag nem fut. Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2a4fd-153">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a4fd-154">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2a4fd-154">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a4fd-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a4fd-155">CommonParameters</span></span>
<span data-ttu-id="2a4fd-156">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2a4fd-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a4fd-157">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a4fd-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a4fd-158">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2a4fd-158">INPUTS</span></span>

### <span data-ttu-id="2a4fd-159">Webhely</span><span class="sxs-lookup"><span data-stu-id="2a4fd-159">Site</span></span>
<span data-ttu-id="2a4fd-160">A ' WebApp ' paraméter elfogadja a "webhely" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="2a4fd-160">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="2a4fd-161">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2a4fd-161">OUTPUTS</span></span>

## <span data-ttu-id="2a4fd-162">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2a4fd-162">NOTES</span></span>

## <span data-ttu-id="2a4fd-163">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2a4fd-163">RELATED LINKS</span></span>

[<span data-ttu-id="2a4fd-164">Get-AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="2a4fd-164">Get-AzureRmWebAppSSLBinding</span></span>](./Get-AzureRmWebAppSSLBinding.md)

[<span data-ttu-id="2a4fd-165">Új – AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="2a4fd-165">New-AzureRmWebAppSSLBinding</span></span>](./New-AzureRmWebAppSSLBinding.md)

[<span data-ttu-id="2a4fd-166">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="2a4fd-166">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="2a4fd-167">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="2a4fd-167">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

