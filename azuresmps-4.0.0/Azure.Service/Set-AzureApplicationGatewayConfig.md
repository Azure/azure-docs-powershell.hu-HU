---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: D7D99AFA-A85E-43DA-9F2F-8FFD34048E00
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7ede675ab58905f102fb9d0029669115acdb9e85
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016429"
---
# <span data-ttu-id="36c66-101">Set-AzureApplicationGatewayConfig</span><span class="sxs-lookup"><span data-stu-id="36c66-101">Set-AzureApplicationGatewayConfig</span></span>

## <span data-ttu-id="36c66-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="36c66-102">SYNOPSIS</span></span>
<span data-ttu-id="36c66-103">Az alkalmazás-átjáró beállítása.</span><span class="sxs-lookup"><span data-stu-id="36c66-103">Configures an application gateway.</span></span>

## <span data-ttu-id="36c66-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="36c66-104">SYNTAX</span></span>

### <span data-ttu-id="36c66-105">Engedélybeállítások</span><span class="sxs-lookup"><span data-stu-id="36c66-105">configFile</span></span>
```
Set-AzureApplicationGatewayConfig -Name <String> -ConfigFile <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="36c66-106">configObject</span><span class="sxs-lookup"><span data-stu-id="36c66-106">configObject</span></span>
```
Set-AzureApplicationGatewayConfig -Name <String> -Config <ApplicationGatewayConfiguration>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="36c66-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="36c66-107">DESCRIPTION</span></span>
<span data-ttu-id="36c66-108">A **set-AzureApplicationGatewayConfig** parancsmag egy alkalmazás-átjárót konfigurál.</span><span class="sxs-lookup"><span data-stu-id="36c66-108">The **Set-AzureApplicationGatewayConfig** cmdlet configures an application gateway.</span></span>

## <span data-ttu-id="36c66-109">Példák</span><span class="sxs-lookup"><span data-stu-id="36c66-109">EXAMPLES</span></span>

### <span data-ttu-id="36c66-110">1. példa: az alkalmazás-átjáró konfigurálása konfigurációs objektum használatával</span><span class="sxs-lookup"><span data-stu-id="36c66-110">Example 1: Configure an application gateway by using a configuration object</span></span>
```
PS C:\> $ConfigReturnObject = Get-AzureApplicationGatewayConfig -Name "ApplicationGateway02"
PS C:\> Set-AzureApplicationGatewayConfig -Name "ApplicationGateway06" -Config $ConfigReturnObject
```

<span data-ttu-id="36c66-111">Az első parancs a **Get-AzureApplicationGatewayConfig** parancsmag használatával kapja meg a ApplicationGateway02 nevű alkalmazás-átjáró konfigurációs objektumát.</span><span class="sxs-lookup"><span data-stu-id="36c66-111">The first command gets the configuration object for the application gateway named ApplicationGateway02 by using the **Get-AzureApplicationGatewayConfig** cmdlet.</span></span>
<span data-ttu-id="36c66-112">A parancs a $ConfigReturnObject változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="36c66-112">The command stores it in the $ConfigReturnObject variable.</span></span>

<span data-ttu-id="36c66-113">A második parancs beállítja a ApplicationGateway06 nevű alkalmazás konfigurációját az $ConfigReturnObject változóban tárolt Application Gateway Configuration objektum használatával.</span><span class="sxs-lookup"><span data-stu-id="36c66-113">The second command sets the configuration for the application named ApplicationGateway06 by using an application gateway configuration object stored in the $ConfigReturnObject variable.</span></span>

### <span data-ttu-id="36c66-114">2. példa: az alkalmazás-átjáró konfigurálása konfigurációs fájllal</span><span class="sxs-lookup"><span data-stu-id="36c66-114">Example 2: Configure an application gateway by using a configuration file</span></span>
```
PS C:\> Set-AzureApplicationGatewayConfig -Name "ApplicationGateway06" -ConfigFile "D:\config.xml"
```

<span data-ttu-id="36c66-115">Ez a parancs beállítja a ApplicationGateway06 nevű alkalmazás konfigurációját a megadott helyen, az Application Gateway konfigurációs fájljával.</span><span class="sxs-lookup"><span data-stu-id="36c66-115">This command sets the configuration for the application named ApplicationGateway06 by using an application gateway configuration file in the specified location.</span></span>

### <span data-ttu-id="36c66-116">3. példa: konfiguráció módosítása konfigurációs objektum használatával</span><span class="sxs-lookup"><span data-stu-id="36c66-116">Example 3: Modify a configuration by using a configuration object</span></span>
```
PS C:\> $ConfigReturnObject = Get-AzureApplicationGatewayConfig -Name "ApplicationGateway06"
PS C:\> $ConfigReturnObject.Config.FrontendPorts[0].Port = 443
PS C:\> $ConfigReturnObject | Set-AzureApplicationGatewayConfig -Name "ApplicationGateway06"
```

<span data-ttu-id="36c66-117">Az első parancs a **Get-AzureApplicationGatewayConfig** parancsmag használatával kapja meg a ApplicationGateway06 nevű alkalmazás-átjáró konfigurációs objektumát.</span><span class="sxs-lookup"><span data-stu-id="36c66-117">The first command gets the configuration object for the application gateway named ApplicationGateway06 by using the **Get-AzureApplicationGatewayConfig** cmdlet.</span></span>
<span data-ttu-id="36c66-118">A parancs a $ConfigReturnObject változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="36c66-118">The command stores it in the $ConfigReturnObject variable.</span></span>

<span data-ttu-id="36c66-119">A második parancs a $ConfigReturnObjectban tárolt objektum egy **port** tulajdonságához rendeli a portszámot.</span><span class="sxs-lookup"><span data-stu-id="36c66-119">The second command assigns a port value to a **Port** property in the object stored in $ConfigReturnObject.</span></span>

<span data-ttu-id="36c66-120">A végleges parancs átadja a frissített $ConfigReturnObject az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="36c66-120">The final command passes the updated $ConfigReturnObject to the current cmdlet.</span></span>

## <span data-ttu-id="36c66-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="36c66-121">PARAMETERS</span></span>

### <span data-ttu-id="36c66-122">-Config</span><span class="sxs-lookup"><span data-stu-id="36c66-122">-Config</span></span>
<span data-ttu-id="36c66-123">Az Application Gateway konfigurációs objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="36c66-123">Specifies an application gateway configuration object.</span></span>
<span data-ttu-id="36c66-124">Ez a parancsmag azt a konfigurációt rendeli hozzá, amelyet ez a paraméter egy alkalmazás-átjáróhoz ad meg.</span><span class="sxs-lookup"><span data-stu-id="36c66-124">This cmdlet assigns the configuration that this parameter specifies to an application gateway.</span></span>

```yaml
Type: ApplicationGatewayConfiguration
Parameter Sets: configObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36c66-125">-Engedélybeállítások</span><span class="sxs-lookup"><span data-stu-id="36c66-125">-ConfigFile</span></span>
<span data-ttu-id="36c66-126">A konfigurációs fájl elérési útját adja meg XML-formátumban az alkalmazás-átjárók számára.</span><span class="sxs-lookup"><span data-stu-id="36c66-126">Specifies the path of a configuration file, in XML format, for an application gateway.</span></span>
<span data-ttu-id="36c66-127">Ez a parancsmag azt a konfigurációt rendeli hozzá, amelyet ez a paraméter egy alkalmazás-átjáróhoz ad meg.</span><span class="sxs-lookup"><span data-stu-id="36c66-127">This cmdlet assigns the configuration that this parameter specifies to an application gateway.</span></span>

```yaml
Type: String
Parameter Sets: configFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36c66-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="36c66-128">-Name</span></span>
<span data-ttu-id="36c66-129">Annak az alkalmazás-átjárónak a nevét adja meg, amelyre a parancsmag konfigurálva van.</span><span class="sxs-lookup"><span data-stu-id="36c66-129">Specifies the name of the application gateway that this cmdlet configures.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36c66-130">-Profil</span><span class="sxs-lookup"><span data-stu-id="36c66-130">-Profile</span></span>
<span data-ttu-id="36c66-131">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="36c66-131">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="36c66-132">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="36c66-132">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36c66-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36c66-133">CommonParameters</span></span>
<span data-ttu-id="36c66-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="36c66-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36c66-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36c66-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36c66-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="36c66-136">INPUTS</span></span>

### <span data-ttu-id="36c66-137">System. string, Microsoft. Azure. Networking. ApplicationGatewayObjectModel. ApplicationGatewayConfiguration</span><span class="sxs-lookup"><span data-stu-id="36c66-137">System.String, Microsoft.Azure.Networking.ApplicationGatewayObjectModel.ApplicationGatewayConfiguration</span></span>

## <span data-ttu-id="36c66-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="36c66-138">OUTPUTS</span></span>

### <span data-ttu-id="36c66-139">Microsoft. WindowsAzure. Management. ApplicationGateway. models. ApplicationGatewayOperationResponse</span><span class="sxs-lookup"><span data-stu-id="36c66-139">Microsoft.WindowsAzure.Management.ApplicationGateway.Models.ApplicationGatewayOperationResponse</span></span>

## <span data-ttu-id="36c66-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="36c66-140">NOTES</span></span>

## <span data-ttu-id="36c66-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="36c66-141">RELATED LINKS</span></span>

[<span data-ttu-id="36c66-142">Get-AzureApplicationGatewayConfig</span><span class="sxs-lookup"><span data-stu-id="36c66-142">Get-AzureApplicationGatewayConfig</span></span>](./Get-AzureApplicationGatewayConfig.md)


