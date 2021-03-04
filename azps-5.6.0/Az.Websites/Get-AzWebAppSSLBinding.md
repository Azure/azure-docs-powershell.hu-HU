---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: EE3D2BA0-32E7-4A37-BCAF-F0E8FAAC43CE
online version: https://docs.microsoft.com/powershell/module/az.websites/get-azwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSSLBinding.md
ms.openlocfilehash: 08a9fbd9798a3fd3b53d7d71aca9ebd607d23164
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101929465"
---
# <span data-ttu-id="2aebc-101">Get-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="2aebc-101">Get-AzWebAppSSLBinding</span></span>

## <span data-ttu-id="2aebc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2aebc-102">SYNOPSIS</span></span>
<span data-ttu-id="2aebc-103">Azure Web App-tanúsítvány SSL-kötést kap.</span><span class="sxs-lookup"><span data-stu-id="2aebc-103">Gets an Azure Web App certificate SSL binding.</span></span>

## <span data-ttu-id="2aebc-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2aebc-104">SYNTAX</span></span>

### <span data-ttu-id="2aebc-105">S1</span><span class="sxs-lookup"><span data-stu-id="2aebc-105">S1</span></span>
```
Get-AzWebAppSSLBinding [[-Name] <String>] [-ResourceGroupName] <String> [-WebAppName] <String>
 [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2aebc-106">S2</span><span class="sxs-lookup"><span data-stu-id="2aebc-106">S2</span></span>
```
Get-AzWebAppSSLBinding [[-Name] <String>] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2aebc-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2aebc-107">DESCRIPTION</span></span>
<span data-ttu-id="2aebc-108">A **Get-AzWebAppSSLBinding** parancsmag ssl-kötést kap az Azure Web Apphoz.</span><span class="sxs-lookup"><span data-stu-id="2aebc-108">The **Get-AzWebAppSSLBinding** cmdlet gets a Secure Sockets Layer (SSL) binding for an Azure Web App.</span></span>
<span data-ttu-id="2aebc-109">Az SSL-kötések a webalkalmazások egy feltöltött tanúsítvánnyal való társítását használják.</span><span class="sxs-lookup"><span data-stu-id="2aebc-109">SSL bindings are used to associate a Web App with an uploaded certificate.</span></span>
<span data-ttu-id="2aebc-110">A webalkalmazások több tanúsítványhoz is kötve lehet.</span><span class="sxs-lookup"><span data-stu-id="2aebc-110">Web Apps can be bound to multiple certificates.</span></span>

## <span data-ttu-id="2aebc-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2aebc-111">EXAMPLES</span></span>

### <span data-ttu-id="2aebc-112">1. példa: SSL-kötések lekérte webalkalmazáshoz</span><span class="sxs-lookup"><span data-stu-id="2aebc-112">Example 1: Get SSL bindings for a Web App</span></span>
```
PS C:\>Get-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp"
```

<span data-ttu-id="2aebc-113">Ez a parancs beolvassa a ContosoWebApp webapp SSL-kötését, amely a ContosoResourceGroup erőforráscsoporthoz van társítva.</span><span class="sxs-lookup"><span data-stu-id="2aebc-113">This command retrieves the SSL bindings for the Web App ContosoWebApp, which is associated with the resource group ContosoResourceGroup.</span></span>

### <span data-ttu-id="2aebc-114">2. példa: Objektumhivatkozás használata a webalkalmazás SSL-kötésének lekértéhez</span><span class="sxs-lookup"><span data-stu-id="2aebc-114">Example 2: Use an object reference to get SSL bindings for a Web App</span></span>
```
PS C:\>$WebApp = Get-AzWebApp -Name "ContosoWebApp"
PS C:\> Get-AzWebAppSSLBinding -WebApp $WebApp
```

<span data-ttu-id="2aebc-115">A példában található parancsok a ContosoWebApp webapp SSL-kötését is megkapják; ebben az esetben azonban a webalkalmazás neve és a társított erőforráscsoport neve helyett objektumhivatkozást használ a szolgáltatás.</span><span class="sxs-lookup"><span data-stu-id="2aebc-115">The commands in this example also get the SSL bindings for the Web App ContosoWebApp; in this case, however, an object reference is used instead of the Web App name and the name of the associated resource group.</span></span>
<span data-ttu-id="2aebc-116">Ezt az objektumhivatkozást a példa első parancsa hozza létre, amely a **Get-AzWebApp** segítségével létrehoz egy objektumhivatkozást a ContosoWebApp nevű webappra.</span><span class="sxs-lookup"><span data-stu-id="2aebc-116">This object reference is created by the first command in the example, which uses **Get-AzWebApp** to create an object reference to the Web App named ContosoWebApp.</span></span>
<span data-ttu-id="2aebc-117">Ezt az objektumhivatkozást egy $WebApp.</span><span class="sxs-lookup"><span data-stu-id="2aebc-117">That object reference is stored in a variable named $WebApp.</span></span>
<span data-ttu-id="2aebc-118">Ezt a változót és a **Get-AzWebAppSSLBinding** parancsmagot a második parancsmag használja az SSL-kötések be szereznie.</span><span class="sxs-lookup"><span data-stu-id="2aebc-118">This variable, and the **Get-AzWebAppSSLBinding** cmdlet, are then used by the second command to get the SSL bindings.</span></span>

## <span data-ttu-id="2aebc-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2aebc-119">PARAMETERS</span></span>

### <span data-ttu-id="2aebc-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2aebc-120">-DefaultProfile</span></span>
<span data-ttu-id="2aebc-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2aebc-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2aebc-122">-Name</span><span class="sxs-lookup"><span data-stu-id="2aebc-122">-Name</span></span>
<span data-ttu-id="2aebc-123">Az SSL-kötés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2aebc-123">Specifies the name of the SSL binding.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2aebc-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2aebc-124">-ResourceGroupName</span></span>
<span data-ttu-id="2aebc-125">Annak az erőforráscsoportnak a neve, amelyhez a tanúsítvány hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="2aebc-125">Specifies the name of the resource group that the certificate is assigned to.</span></span>
<span data-ttu-id="2aebc-126">Ugyanabban a parancsban nem használhatja az *ResourceGroupName* és a *WebApp* paramétert.</span><span class="sxs-lookup"><span data-stu-id="2aebc-126">You cannot use the *ResourceGroupName* parameter and the *WebApp* parameter in the same command.</span></span>

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

### <span data-ttu-id="2aebc-127">-Slot</span><span class="sxs-lookup"><span data-stu-id="2aebc-127">-Slot</span></span>
<span data-ttu-id="2aebc-128">Egy webalkalmazás-telepítőhelyet ad meg.</span><span class="sxs-lookup"><span data-stu-id="2aebc-128">Specifies a Web App deployment slot.</span></span>
<span data-ttu-id="2aebc-129">Telepítési hely letelepítéséhez használja a Get-AzWebAppSlot parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="2aebc-129">To get a deployment slot, use the Get-AzWebAppSlot cmdlet.</span></span>

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

### <span data-ttu-id="2aebc-130">-WebApp</span><span class="sxs-lookup"><span data-stu-id="2aebc-130">-WebApp</span></span>
<span data-ttu-id="2aebc-131">Egy webalkalmazást ad meg.</span><span class="sxs-lookup"><span data-stu-id="2aebc-131">Specifies a Web App.</span></span>
<span data-ttu-id="2aebc-132">Webalkalmazás lekérte a Get-AzWebApp parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="2aebc-132">To get a Web App, use the Get-AzWebApp cmdlet.</span></span>

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

### <span data-ttu-id="2aebc-133">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="2aebc-133">-WebAppName</span></span>
<span data-ttu-id="2aebc-134">Annak a webalkalmazásnak a nevét adja meg, amelyből ez a parancsmag SSL-kötéseket kap.</span><span class="sxs-lookup"><span data-stu-id="2aebc-134">Specifies the name of the Web App that this cmdlet gets SSL bindings from.</span></span>
<span data-ttu-id="2aebc-135">Ugyanabban a parancsban nem használhatja a *WebAppName* és a *WebApp* paramétert.</span><span class="sxs-lookup"><span data-stu-id="2aebc-135">You cannot use the *WebAppName* parameter and the *WebApp* parameter in the same command.</span></span>

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

### <span data-ttu-id="2aebc-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2aebc-136">CommonParameters</span></span>
<span data-ttu-id="2aebc-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2aebc-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2aebc-138">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2aebc-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2aebc-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2aebc-139">INPUTS</span></span>

### <span data-ttu-id="2aebc-140">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="2aebc-140">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="2aebc-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2aebc-141">OUTPUTS</span></span>

### <span data-ttu-id="2aebc-142">Microsoft.Azure.Management.WebSites.Models.HostNameSslState</span><span class="sxs-lookup"><span data-stu-id="2aebc-142">Microsoft.Azure.Management.WebSites.Models.HostNameSslState</span></span>

## <span data-ttu-id="2aebc-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2aebc-143">NOTES</span></span>

## <span data-ttu-id="2aebc-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2aebc-144">RELATED LINKS</span></span>

[<span data-ttu-id="2aebc-145">New-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="2aebc-145">New-AzWebAppSSLBinding</span></span>](./New-AzWebAppSSLBinding.md)

[<span data-ttu-id="2aebc-146">Remove-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="2aebc-146">Remove-AzWebAppSSLBinding</span></span>](./Remove-AzWebAppSSLBinding.md)

[<span data-ttu-id="2aebc-147">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="2aebc-147">Get-AzWebApp</span></span>](./Get-AzWebApp.md)


