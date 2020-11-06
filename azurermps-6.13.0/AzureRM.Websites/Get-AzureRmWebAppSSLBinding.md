---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: EE3D2BA0-32E7-4A37-BCAF-F0E8FAAC43CE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSSLBinding.md
ms.openlocfilehash: ae97bc08e5ba8c801e3bf5126c6e48dfb7910751
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93491826"
---
# <span data-ttu-id="94674-101">Get-AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="94674-101">Get-AzureRmWebAppSSLBinding</span></span>

## <span data-ttu-id="94674-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="94674-102">SYNOPSIS</span></span>
<span data-ttu-id="94674-103">Az Azure Web App tanúsítványának SSL-kötését kapja.</span><span class="sxs-lookup"><span data-stu-id="94674-103">Gets an Azure Web App certificate SSL binding.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="94674-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="94674-104">SYNTAX</span></span>

### <span data-ttu-id="94674-105">S1</span><span class="sxs-lookup"><span data-stu-id="94674-105">S1</span></span>
```
Get-AzureRmWebAppSSLBinding [[-Name] <String>] [-ResourceGroupName] <String> [-WebAppName] <String>
 [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94674-106">S2</span><span class="sxs-lookup"><span data-stu-id="94674-106">S2</span></span>
```
Get-AzureRmWebAppSSLBinding [[-Name] <String>] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="94674-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="94674-107">DESCRIPTION</span></span>
<span data-ttu-id="94674-108">A **Get-AzureRmWebAppSSLBinding** parancsmag Secure Sockets Layer (SSL) kötést kap az Azure Web App alkalmazáshoz.</span><span class="sxs-lookup"><span data-stu-id="94674-108">The **Get-AzureRmWebAppSSLBinding** cmdlet gets a Secure Sockets Layer (SSL) binding for an Azure Web App.</span></span>
<span data-ttu-id="94674-109">Az SSL-kötések a webalkalmazások feltöltött tanúsítványsal való társítására szolgálnak.</span><span class="sxs-lookup"><span data-stu-id="94674-109">SSL bindings are used to associate a Web App with an uploaded certificate.</span></span>
<span data-ttu-id="94674-110">A webes alkalmazások több tanúsítványhoz is kötve lehetnek.</span><span class="sxs-lookup"><span data-stu-id="94674-110">Web Apps can be bound to multiple certificates.</span></span>

## <span data-ttu-id="94674-111">Példák</span><span class="sxs-lookup"><span data-stu-id="94674-111">EXAMPLES</span></span>

### <span data-ttu-id="94674-112">Példa 1: SSL-kötések beszerzése egy webalkalmazáshoz</span><span class="sxs-lookup"><span data-stu-id="94674-112">Example 1: Get SSL bindings for a Web App</span></span>
```
PS C:\>Get-AzureRmWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp"
```

<span data-ttu-id="94674-113">Ez a parancs beolvassa a Web App ContosoWebApp az erőforráscsoport ContosoResourceGroup társított SSL-kötéseit.</span><span class="sxs-lookup"><span data-stu-id="94674-113">This command retrieves the SSL bindings for the Web App ContosoWebApp, which is associated with the resource group ContosoResourceGroup.</span></span>

### <span data-ttu-id="94674-114">2. példa: az SSL-kötések beszerzése egy webalkalmazáshoz objektum-hivatkozás használatával</span><span class="sxs-lookup"><span data-stu-id="94674-114">Example 2: Use an object reference to get SSL bindings for a Web App</span></span>
```
PS C:\>$WebApp = Get-AzureRmWebApp -Name "ContosoWebApp"
PS C:\> Get-AzureRmWebAppSSLBinding -WebApp $WebApp
```

<span data-ttu-id="94674-115">Az ebben a példában szereplő parancsok a Web App ContosoWebApp tartozó SSL-kötéseket is megkapják; Ebben az esetben azonban a Web App neve és a hozzá tartozó erőforráscsoport neve helyett egy objektum-hivatkozás van használatban.</span><span class="sxs-lookup"><span data-stu-id="94674-115">The commands in this example also get the SSL bindings for the Web App ContosoWebApp; in this case, however, an object reference is used instead of the Web App name and the name of the associated resource group.</span></span>
<span data-ttu-id="94674-116">Ezt az objektumot a példa első parancsa hozza létre, amely a **Get-AzureRmWebApp** használatával hozza létre az objektum hivatkozását a ContosoWebApp nevű webalkalmazáshoz.</span><span class="sxs-lookup"><span data-stu-id="94674-116">This object reference is created by the first command in the example, which uses **Get-AzureRmWebApp** to create an object reference to the Web App named ContosoWebApp.</span></span>
<span data-ttu-id="94674-117">Az objektum hivatkozása $WebApp nevű változóban tárolódik.</span><span class="sxs-lookup"><span data-stu-id="94674-117">That object reference is stored in a variable named $WebApp.</span></span>
<span data-ttu-id="94674-118">Ezt a változót és a **Get-AzureRmWebAppSSLBinding** parancsmagot a második parancs használja az SSL-kötések beszerzéséhez.</span><span class="sxs-lookup"><span data-stu-id="94674-118">This variable, and the **Get-AzureRmWebAppSSLBinding** cmdlet, are then used by the second command to get the SSL bindings.</span></span>

## <span data-ttu-id="94674-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="94674-119">PARAMETERS</span></span>

### <span data-ttu-id="94674-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94674-120">-DefaultProfile</span></span>
<span data-ttu-id="94674-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="94674-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="94674-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="94674-122">-Name</span></span>
<span data-ttu-id="94674-123">Az SSL-kötés nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="94674-123">Specifies the name of the SSL binding.</span></span>

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

### <span data-ttu-id="94674-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94674-124">-ResourceGroupName</span></span>
<span data-ttu-id="94674-125">Annak az erőforráscsoportnek a neve, amelyhez a tanúsítvány van rendelve.</span><span class="sxs-lookup"><span data-stu-id="94674-125">Specifies the name of the resource group that the certificate is assigned to.</span></span>
<span data-ttu-id="94674-126">A *ResourceGroupName* paraméter és a *WebApp* paraméter nem használható ugyanabban a parancsban.</span><span class="sxs-lookup"><span data-stu-id="94674-126">You cannot use the *ResourceGroupName* parameter and the *WebApp* parameter in the same command.</span></span>

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

### <span data-ttu-id="94674-127">-Slot</span><span class="sxs-lookup"><span data-stu-id="94674-127">-Slot</span></span>
<span data-ttu-id="94674-128">Egy webalkalmazás-telepítő bővítőhelyet ad meg.</span><span class="sxs-lookup"><span data-stu-id="94674-128">Specifies a Web App deployment slot.</span></span>
<span data-ttu-id="94674-129">Ha egy központi telepítő bővítőhelyet szeretne használni, használja az Get-AzureRMWebAppSlot parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="94674-129">To get a deployment slot, use the Get-AzureRMWebAppSlot cmdlet.</span></span>

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

### <span data-ttu-id="94674-130">-WebApp</span><span class="sxs-lookup"><span data-stu-id="94674-130">-WebApp</span></span>
<span data-ttu-id="94674-131">Egy webalkalmazást ad meg.</span><span class="sxs-lookup"><span data-stu-id="94674-131">Specifies a Web App.</span></span>
<span data-ttu-id="94674-132">Ha egy webalkalmazást szeretne beszerezni, használja az Get-AzureRmWebApp parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="94674-132">To get a Web App, use the Get-AzureRmWebApp cmdlet.</span></span>

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

### <span data-ttu-id="94674-133">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="94674-133">-WebAppName</span></span>
<span data-ttu-id="94674-134">Annak a webalkalmazásnak a nevét adja meg, amelynek a parancsmagja SSL-kötést kap.</span><span class="sxs-lookup"><span data-stu-id="94674-134">Specifies the name of the Web App that this cmdlet gets SSL bindings from.</span></span>
<span data-ttu-id="94674-135">A *WebAppName* paraméter és a *WebApp* paraméter nem használható ugyanabban a parancsban.</span><span class="sxs-lookup"><span data-stu-id="94674-135">You cannot use the *WebAppName* parameter and the *WebApp* parameter in the same command.</span></span>

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

### <span data-ttu-id="94674-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94674-136">CommonParameters</span></span>
<span data-ttu-id="94674-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="94674-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94674-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94674-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94674-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="94674-139">INPUTS</span></span>

### <span data-ttu-id="94674-140">Microsoft. Azure. Management. WebSites. models. site</span><span class="sxs-lookup"><span data-stu-id="94674-140">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="94674-141">Paraméterek: WebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="94674-141">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="94674-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="94674-142">OUTPUTS</span></span>

### <span data-ttu-id="94674-143">Microsoft. Azure. Management. WebSites. models. HostNameSslState</span><span class="sxs-lookup"><span data-stu-id="94674-143">Microsoft.Azure.Management.WebSites.Models.HostNameSslState</span></span>

## <span data-ttu-id="94674-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="94674-144">NOTES</span></span>

## <span data-ttu-id="94674-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="94674-145">RELATED LINKS</span></span>

[<span data-ttu-id="94674-146">Új – AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="94674-146">New-AzureRmWebAppSSLBinding</span></span>](./New-AzureRmWebAppSSLBinding.md)

[<span data-ttu-id="94674-147">Remove-AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="94674-147">Remove-AzureRmWebAppSSLBinding</span></span>](./Remove-AzureRmWebAppSSLBinding.md)

[<span data-ttu-id="94674-148">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="94674-148">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)


