---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 3AB3D398-E5DB-4214-BA27-6E3B7D225550
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/remove-azwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppSSLBinding.md
ms.openlocfilehash: bed5cb961fd39975b3f10debe8791a418fd5dcda
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466986"
---
# <span data-ttu-id="b2977-101">Remove-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="b2977-101">Remove-AzWebAppSSLBinding</span></span>

## <span data-ttu-id="b2977-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2977-102">SYNOPSIS</span></span>
<span data-ttu-id="b2977-103">Eltávolít egy SSL-kötést egy feltöltött tanúsítványból.</span><span class="sxs-lookup"><span data-stu-id="b2977-103">Removes an SSL binding from an uploaded certificate.</span></span>

## <span data-ttu-id="b2977-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b2977-104">SYNTAX</span></span>

### <span data-ttu-id="b2977-105">S1</span><span class="sxs-lookup"><span data-stu-id="b2977-105">S1</span></span>
```
Remove-AzWebAppSSLBinding [-Name] <String> [[-DeleteCertificate] <Boolean>] [-Force]
 [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2977-106">S2</span><span class="sxs-lookup"><span data-stu-id="b2977-106">S2</span></span>
```
Remove-AzWebAppSSLBinding [-Name] <String> [[-DeleteCertificate] <Boolean>] [-Force] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2977-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b2977-107">DESCRIPTION</span></span>
<span data-ttu-id="b2977-108">A **Remove-AzWebAppSSLBinding** parancsmag eltávolítja az SSL-kötéseket az Azure Web Appból.</span><span class="sxs-lookup"><span data-stu-id="b2977-108">The **Remove-AzWebAppSSLBinding** cmdlet removes a Secure Sockets Layer (SSL) binding from an Azure Web App.</span></span>
<span data-ttu-id="b2977-109">Az SSL-kötések a webalkalmazások tanúsítványhoz való társítását használják.</span><span class="sxs-lookup"><span data-stu-id="b2977-109">SSL bindings are used to associate a Web App with a certificate.</span></span>

## <span data-ttu-id="b2977-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b2977-110">EXAMPLES</span></span>

### <span data-ttu-id="b2977-111">1. példa: SSL-kötés eltávolítása webalkalmazáshoz</span><span class="sxs-lookup"><span data-stu-id="b2977-111">Example 1: Remove an SSL binding for a web app</span></span>
```
PS C:\>Remove-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Name "www.contoso.com"
```

<span data-ttu-id="b2977-112">Ez a parancs eltávolítja a ContosoWebApp webapp SSL-kötését.</span><span class="sxs-lookup"><span data-stu-id="b2977-112">This command removes the SSL binding for the web app ContosoWebApp.</span></span>
<span data-ttu-id="b2977-113">Mivel a *DeleteCertificate* paraméter nem szerepel a paraméterben, a tanúsítvány törlődik, ha már nincs SSL-kötése.</span><span class="sxs-lookup"><span data-stu-id="b2977-113">Since the *DeleteCertificate* parameter is not included, the certificate will be deleted if it no longer has any SSL bindings.</span></span>

### <span data-ttu-id="b2977-114">2. példa: SSL-kötés eltávolítása a tanúsítvány eltávolítása nélkül</span><span class="sxs-lookup"><span data-stu-id="b2977-114">Example 2: Remove an SSL binding without removing the certificate</span></span>
```
PS C:\>Remove-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Name "www.contoso.com" -DeleteCertificate $False
```

<span data-ttu-id="b2977-115">Az 1. példához hasonlóan ez a parancs a ContosoWebApp webapp SSL-kötését is eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="b2977-115">Similar to Example 1, this command also removes the SSL binding for the Web App ContosoWebApp.</span></span>
<span data-ttu-id="b2977-116">Ebben az esetben azonban szerepel a *DeleteCertificate* paraméter, és a paraméter értéke $False.</span><span class="sxs-lookup"><span data-stu-id="b2977-116">In this case, however, the *DeleteCertificate* parameter is included, and the parameter value is set to $False.</span></span>
<span data-ttu-id="b2977-117">Ez azt jelenti, hogy a tanúsítvány nem törlődik, függetlenül attól, hogy rendelkezik-e SSL-kötéssel.</span><span class="sxs-lookup"><span data-stu-id="b2977-117">That means that the certificate will not be deleted regardless of whether it has any SSL bindings or not.</span></span>

### <span data-ttu-id="b2977-118">3. példa: Ssl-kötés eltávolítása objektumhivatkozással</span><span class="sxs-lookup"><span data-stu-id="b2977-118">Example 3: Use an object reference to remove an SSL binding</span></span>
```
PS C:\>$WebApp = Get-AzWebApp -Name "ContosoWebApp"
PS C:\> Remove-AzWebAppSSLBinding -WebApp $WebApp -Name "www.contoso.com"
```

<span data-ttu-id="b2977-119">Ebben a példában egy objektumhivatkozást használtunk a Web App webhelyére a webalkalmazás SSL-kötésének eltávolításához.</span><span class="sxs-lookup"><span data-stu-id="b2977-119">This example uses an object reference to the Web App website to remove the SSL binding for a Web App.</span></span>
<span data-ttu-id="b2977-120">Az első parancs a Get-AzWebApp parancsmag használatával hoz létre egy, a ContosoWebApp nevű webalkalmazásra való hivatkozást.</span><span class="sxs-lookup"><span data-stu-id="b2977-120">The first command uses the Get-AzWebApp cmdlet to create an object reference to the Web App named ContosoWebApp.</span></span>
<span data-ttu-id="b2977-121">Ezt az objektumhivatkozást egy $WebApp.</span><span class="sxs-lookup"><span data-stu-id="b2977-121">That object reference is stored in a variable named $WebApp.</span></span>
<span data-ttu-id="b2977-122">A második parancs az SSL-kötés eltávolításához az objektumhivatkozást és a **Remove-AzWebAppSSLBinding** parancsmagot használja.</span><span class="sxs-lookup"><span data-stu-id="b2977-122">The second command uses the object reference and the **Remove-AzWebAppSSLBinding** cmdlet to remove the SSL binding.</span></span>

## <span data-ttu-id="b2977-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b2977-123">PARAMETERS</span></span>

### <span data-ttu-id="b2977-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2977-124">-DefaultProfile</span></span>
<span data-ttu-id="b2977-125">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b2977-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b2977-126">-DeleteCertificate</span><span class="sxs-lookup"><span data-stu-id="b2977-126">-DeleteCertificate</span></span>
<span data-ttu-id="b2977-127">Azt a műveletet adja meg, amelyet akkor kell alkalmazni, ha az eltávolított SSL-kötés az egyetlen kötés, amelyet a tanúsítvány használ.</span><span class="sxs-lookup"><span data-stu-id="b2977-127">Specifies the action to take place if the SSL binding being removed is the only binding used by the certificate.</span></span>
<span data-ttu-id="b2977-128">Ha *a DeleteCertificate* $False, a tanúsítvány nem törlődik a kötés törlésekor.</span><span class="sxs-lookup"><span data-stu-id="b2977-128">If *DeleteCertificate* is set to $False, the certificate will not be deleted when the binding is deleted.</span></span>
<span data-ttu-id="b2977-129">Ha *a DeleteCertificate* $True vagy nem szerepel a parancsban, a tanúsítvány az SSL-kötéssel együtt törlődik.</span><span class="sxs-lookup"><span data-stu-id="b2977-129">If *DeleteCertificate* is set to $True or is not included in the command, the certificate will be deleted along with the SSL binding.</span></span>
<span data-ttu-id="b2977-130">A tanúsítvány csak akkor törlődik, ha az eltávolított SSL-kötés az egyetlen kötés, amelyet a tanúsítvány használ.</span><span class="sxs-lookup"><span data-stu-id="b2977-130">The certificate will only be deleted if the SSL binding being removed is the only binding used by the certificate.</span></span>
<span data-ttu-id="b2977-131">Ha a tanúsítványnak több kötése van, a rendszer nem távolítja el a tanúsítványt a *DeleteCertificate* paraméter értékétől függetlenül.</span><span class="sxs-lookup"><span data-stu-id="b2977-131">If the certificate has more than one binding, the certificate will not be removed regardless of the value of the *DeleteCertificate* parameter.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2977-132">-Force</span><span class="sxs-lookup"><span data-stu-id="b2977-132">-Force</span></span>
<span data-ttu-id="b2977-133">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="b2977-133">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2977-134">-Name</span><span class="sxs-lookup"><span data-stu-id="b2977-134">-Name</span></span>
<span data-ttu-id="b2977-135">A webalkalmazás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b2977-135">Specifies the name of the Web App.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2977-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2977-136">-ResourceGroupName</span></span>
<span data-ttu-id="b2977-137">Annak az erőforráscsoportnak a neve, amelyhez a tanúsítvány hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="b2977-137">Specifies the name of the resource group that the certificate is assigned to.</span></span>
<span data-ttu-id="b2977-138">Ugyanabban a parancsban nem használhatja az *ResourceGroupName* és a *WebApp* paramétert.</span><span class="sxs-lookup"><span data-stu-id="b2977-138">You cannot use the *ResourceGroupName* parameter and the *WebApp* parameter in the same command.</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2977-139">-Slot</span><span class="sxs-lookup"><span data-stu-id="b2977-139">-Slot</span></span>
<span data-ttu-id="b2977-140">A Web App telepítési helyének megadása.</span><span class="sxs-lookup"><span data-stu-id="b2977-140">Specifies the Web App deployment slot.</span></span>
<span data-ttu-id="b2977-141">Telepítési hely letelepítéséhez használja a Get-AzWebAppSlot parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="b2977-141">To get a deployment slot, use the Get-AzWebAppSlot cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2977-142">-WebApp</span><span class="sxs-lookup"><span data-stu-id="b2977-142">-WebApp</span></span>
<span data-ttu-id="b2977-143">Egy webalkalmazást ad meg.</span><span class="sxs-lookup"><span data-stu-id="b2977-143">Specifies a Web App.</span></span>
<span data-ttu-id="b2977-144">Webalkalmazás lekérte a Get-AzWebApp parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="b2977-144">To get a Web App, use the Get-AzWebApp cmdlet.</span></span>
<span data-ttu-id="b2977-145">A *WebApp paraméter* nem használható ugyanabban a parancsban, mint az *ResourceGroupName* és/vagy a *WebAppName paraméter.*</span><span class="sxs-lookup"><span data-stu-id="b2977-145">You cannot use the *WebApp* parameter in the same command as the *ResourceGroupName* parameter and/or the *WebAppName*.</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b2977-146">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="b2977-146">-WebAppName</span></span>
<span data-ttu-id="b2977-147">A webalkalmazás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b2977-147">Specifies the name of the Web App.</span></span>
<span data-ttu-id="b2977-148">Ugyanabban a parancsban nem használhatja a *WebAppName* és a *WebApp* paramétert.</span><span class="sxs-lookup"><span data-stu-id="b2977-148">You cannot use the *WebAppName* parameter and the *WebApp* parameter in the same command.</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2977-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b2977-149">-Confirm</span></span>
<span data-ttu-id="b2977-150">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="b2977-150">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2977-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2977-151">-WhatIf</span></span>
<span data-ttu-id="b2977-152">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="b2977-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b2977-153">A parancsmag nem fut. A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="b2977-153">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b2977-154">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b2977-154">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2977-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2977-155">CommonParameters</span></span>
<span data-ttu-id="b2977-156">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2977-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2977-157">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2977-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2977-158">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b2977-158">INPUTS</span></span>

### <span data-ttu-id="b2977-159">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="b2977-159">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="b2977-160">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b2977-160">OUTPUTS</span></span>

### <span data-ttu-id="b2977-161">System.Void</span><span class="sxs-lookup"><span data-stu-id="b2977-161">System.Void</span></span>

## <span data-ttu-id="b2977-162">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b2977-162">NOTES</span></span>

## <span data-ttu-id="b2977-163">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b2977-163">RELATED LINKS</span></span>

[<span data-ttu-id="b2977-164">Get-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="b2977-164">Get-AzWebAppSSLBinding</span></span>](./Get-AzWebAppSSLBinding.md)

[<span data-ttu-id="b2977-165">New-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="b2977-165">New-AzWebAppSSLBinding</span></span>](./New-AzWebAppSSLBinding.md)

[<span data-ttu-id="b2977-166">Get-AzWebAppszaj</span><span class="sxs-lookup"><span data-stu-id="b2977-166">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="b2977-167">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="b2977-167">Get-AzWebApp</span></span>](./Get-AzWebApp.md)


