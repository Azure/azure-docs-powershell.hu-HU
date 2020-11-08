---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: 50B83AEC-1B32-4089-9804-D388677C3F7E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7388841c48f2f7c6ba0752748b245cce1f8b5c4e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016092"
---
# <span data-ttu-id="7e288-101">Remove-AzureTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="7e288-101">Remove-AzureTrafficManagerEndpoint</span></span>

## <span data-ttu-id="7e288-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7e288-102">SYNOPSIS</span></span>
<span data-ttu-id="7e288-103">Végpont eltávolítása a forgalomirányító profiljából.</span><span class="sxs-lookup"><span data-stu-id="7e288-103">Removes an endpoint from a Traffic Manager profile.</span></span>

## <span data-ttu-id="7e288-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7e288-104">SYNTAX</span></span>

```
Remove-AzureTrafficManagerEndpoint -DomainName <String> [-Force]
 -TrafficManagerProfile <IProfileWithDefinition> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="7e288-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7e288-105">DESCRIPTION</span></span>
<span data-ttu-id="7e288-106">A **Remove-AzureTrafficManagerEndpoint** parancsmag a Microsoft Azure Traffic Manager-profilból távolítja el a végpontot.</span><span class="sxs-lookup"><span data-stu-id="7e288-106">The **Remove-AzureTrafficManagerEndpoint** cmdlet removes an endpoint from a Microsoft Azure Traffic Manager profile.</span></span>
<span data-ttu-id="7e288-107">Miután eltávolított egy végpontot, átadja az eredményt a **set-AzureTrafficManagerProfile** parancsmagnak a pipeline operátor használatával.</span><span class="sxs-lookup"><span data-stu-id="7e288-107">After you remove an endpoint, pass the result to the **Set-AzureTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="7e288-108">Ez a parancsmag az Azure-hoz csatlakozik a módosítások mentéséhez.</span><span class="sxs-lookup"><span data-stu-id="7e288-108">That cmdlet connects to Azure to save your changes.</span></span>

## <span data-ttu-id="7e288-109">Példák</span><span class="sxs-lookup"><span data-stu-id="7e288-109">EXAMPLES</span></span>

### <span data-ttu-id="7e288-110">Példa 1: végpont eltávolítása egy profilból</span><span class="sxs-lookup"><span data-stu-id="7e288-110">Example 1: Remove an endpoint from a profile</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzureTrafficManagerProfile -Name "ContosoProfile"
PS C:\> Remove-AzureTrafficManagerEndpoint -TrafficManagerProfile $TrafficManagerProfile -DomainName "Contoso02App.cloudapp.net" | Set-AzureTrafficManagerProfile
```

<span data-ttu-id="7e288-111">Az első parancs a **Get-AzureTrafficManagerProfile** parancsmagot használja a ContosoProfile nevű profil beolvasásához, majd a $TrafficManagerProfile változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="7e288-111">The first command uses the **Get-AzureTrafficManagerProfile** cmdlet to get the profile named ContosoProfile, and then stores it in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="7e288-112">A második parancs eltávolítja azt a végpontot, amelynek a tartományneve Contoso02App.cloudapp.net a $TrafficManagerProfileban tárolt forgalomirányítási profilból.</span><span class="sxs-lookup"><span data-stu-id="7e288-112">The second command removes an endpoint that has the domain name Contoso02App.cloudapp.net from the Traffic Manager profile that is stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="7e288-113">A parancs átadja a profil objektumnak a **set-AzureTrafficManagerProfile** parancsmagot az Azure-hoz való csatlakozáshoz a módosítások mentéséhez.</span><span class="sxs-lookup"><span data-stu-id="7e288-113">The command passes the profile object to the **Set-AzureTrafficManagerProfile** cmdlet to connect to Azure to save your changes.</span></span>

## <span data-ttu-id="7e288-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7e288-114">PARAMETERS</span></span>

### <span data-ttu-id="7e288-115">-Tartománynév</span><span class="sxs-lookup"><span data-stu-id="7e288-115">-DomainName</span></span>
<span data-ttu-id="7e288-116">Az eltávolítandó végpont tartománynevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7e288-116">Specifies the domain name of the endpoint to remove.</span></span>

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

### <span data-ttu-id="7e288-117">-Force</span><span class="sxs-lookup"><span data-stu-id="7e288-117">-Force</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e288-118">-Profil</span><span class="sxs-lookup"><span data-stu-id="7e288-118">-Profile</span></span>
<span data-ttu-id="7e288-119">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="7e288-119">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="7e288-120">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="7e288-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7e288-121">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7e288-121">-TrafficManagerProfile</span></span>
<span data-ttu-id="7e288-122">Annak a Traffic Manager-profil objektumnak a meghatározása, amelyből el szeretné távolítani a végpontot.</span><span class="sxs-lookup"><span data-stu-id="7e288-122">Specifies the Traffic Manager profile object from which to remove the endpoint.</span></span>

```yaml
Type: IProfileWithDefinition
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7e288-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e288-123">CommonParameters</span></span>
<span data-ttu-id="7e288-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7e288-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e288-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e288-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e288-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7e288-126">INPUTS</span></span>

## <span data-ttu-id="7e288-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7e288-127">OUTPUTS</span></span>

### <span data-ttu-id="7e288-128">Microsoft. WindowsAzure. Command. Utilities. TrafficManager. models. IProfileWithDefinition</span><span class="sxs-lookup"><span data-stu-id="7e288-128">Microsoft.WindowsAzure.Commands.Utilities.TrafficManager.Models.IProfileWithDefinition</span></span>
<span data-ttu-id="7e288-129">Ez a parancsmag a Traffic Manager profil objektumát hozza létre, amely a frissített profillal kapcsolatos információkat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="7e288-129">This cmdlet generates a Traffic Manager profile object, which contains information about the updated profile.</span></span>

## <span data-ttu-id="7e288-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7e288-130">NOTES</span></span>

## <span data-ttu-id="7e288-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7e288-131">RELATED LINKS</span></span>

[<span data-ttu-id="7e288-132">Add-AzureTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="7e288-132">Add-AzureTrafficManagerEndpoint</span></span>](./Add-AzureTrafficManagerEndpoint.md)

[<span data-ttu-id="7e288-133">Set-AzureTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="7e288-133">Set-AzureTrafficManagerEndpoint</span></span>](./Set-AzureTrafficManagerEndpoint.md)

[<span data-ttu-id="7e288-134">Get-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7e288-134">Get-AzureTrafficManagerProfile</span></span>](./Get-AzureTrafficManagerProfile.md)

[<span data-ttu-id="7e288-135">Set-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7e288-135">Set-AzureTrafficManagerProfile</span></span>](./Set-AzureTrafficManagerProfile.md)


