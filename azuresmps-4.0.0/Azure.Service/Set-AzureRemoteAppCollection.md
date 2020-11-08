---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 14B4050D-3597-4760-A152-82617B88078D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 291ea94bbdfff1da8d658074ebfb72df8943f0e8
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016053"
---
# <span data-ttu-id="3c83e-101">Set-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="3c83e-101">Set-AzureRemoteAppCollection</span></span>

## <span data-ttu-id="3c83e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3c83e-102">SYNOPSIS</span></span>
<span data-ttu-id="3c83e-103">Egy RemoteApp-gyűjtemény tulajdonságait állítja be.</span><span class="sxs-lookup"><span data-stu-id="3c83e-103">Sets the properties of a RemoteApp collection.</span></span>

## <span data-ttu-id="3c83e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3c83e-104">SYNTAX</span></span>

### <span data-ttu-id="3c83e-105">DescriptionOnly (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3c83e-105">DescriptionOnly (Default)</span></span>
```
Set-AzureRemoteAppCollection [-CollectionName] <String> -Description <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="3c83e-106">PlanOnly</span><span class="sxs-lookup"><span data-stu-id="3c83e-106">PlanOnly</span></span>
```
Set-AzureRemoteAppCollection [-CollectionName] <String> -Plan <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="3c83e-107">DomainJoined</span><span class="sxs-lookup"><span data-stu-id="3c83e-107">DomainJoined</span></span>
```
Set-AzureRemoteAppCollection [-CollectionName] <String> -Credential <PSCredential> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="3c83e-108">RdpPropertyOnly</span><span class="sxs-lookup"><span data-stu-id="3c83e-108">RdpPropertyOnly</span></span>
```
Set-AzureRemoteAppCollection [-CollectionName] <String> -CustomRdpProperty <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="3c83e-109">AclLevelOnly</span><span class="sxs-lookup"><span data-stu-id="3c83e-109">AclLevelOnly</span></span>
```
Set-AzureRemoteAppCollection [-CollectionName] <String> -AclLevel <CollectionAclLevel>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="3c83e-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="3c83e-110">DESCRIPTION</span></span>
<span data-ttu-id="3c83e-111">A **set-AzureRemoteAppCollection** parancsmag az Azure RemoteApp-gyűjtemény tulajdonságait állítja be.</span><span class="sxs-lookup"><span data-stu-id="3c83e-111">The **Set-AzureRemoteAppCollection** cmdlet sets the properties of an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="3c83e-112">Példák</span><span class="sxs-lookup"><span data-stu-id="3c83e-112">EXAMPLES</span></span>

## <span data-ttu-id="3c83e-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3c83e-113">PARAMETERS</span></span>

### <span data-ttu-id="3c83e-114">-AclLevel</span><span class="sxs-lookup"><span data-stu-id="3c83e-114">-AclLevel</span></span>
<span data-ttu-id="3c83e-115">A gyűjtemény hozzáférés-vezérlési lista (ACL) szintjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3c83e-115">Specifies the access control list (ACL) level for the collection.</span></span>
<span data-ttu-id="3c83e-116">A paraméter elfogadható értékei a következők: gyűjtemény és alkalmazás.</span><span class="sxs-lookup"><span data-stu-id="3c83e-116">The acceptable values for this parameter are: Collection and Application.</span></span>

```yaml
Type: CollectionAclLevel
Parameter Sets: AclLevelOnly
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c83e-117">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="3c83e-117">-CollectionName</span></span>
<span data-ttu-id="3c83e-118">Az Azure RemoteApp-gyűjtemény nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3c83e-118">Specifies the name of the Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c83e-119">-Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="3c83e-119">-Credential</span></span>
<span data-ttu-id="3c83e-120">Megadja egy olyan szolgáltatásfiók hitelesítő adatait, amely engedéllyel rendelkezik az Azure RemoteApp kiszolgálókhoz való csatlakozáshoz a tartományához.</span><span class="sxs-lookup"><span data-stu-id="3c83e-120">Specifies the credentials of a service account that has permission to join the Azure RemoteApp servers to your domain.</span></span>
<span data-ttu-id="3c83e-121">Ha **PSCredential** objektumot szeretne beolvasni, használja a **Get-hitelesítőadat** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="3c83e-121">To obtain a **PSCredential** object, use the **Get-Credential** cmdlet.</span></span>

```yaml
Type: PSCredential
Parameter Sets: DomainJoined
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c83e-122">-CustomRdpProperty</span><span class="sxs-lookup"><span data-stu-id="3c83e-122">-CustomRdpProperty</span></span>
<span data-ttu-id="3c83e-123">Az RDP-tulajdonságokat adja meg, amelyek segítségével konfigurálhatók a meghajtó átirányítása és az egyéb beállítások.</span><span class="sxs-lookup"><span data-stu-id="3c83e-123">Specifies custom Remote Desktop Protocol (RDP) properties which can be used to configure drive redirection and other settings.</span></span> <span data-ttu-id="3c83e-124">További információt az [RDP-beállítások a Windows Server Remote Desktop Services szolgáltatáshoz](https://technet.microsoft.com/library/ff393699(v=ws.10).aspx) című témakörben talál `(https://technet.microsoft.com/library/ff393699(v=ws.10).aspx)` .  </span><span class="sxs-lookup"><span data-stu-id="3c83e-124">See [RDP Settings for Remote Desktop Services in Windows Server](https://technet.microsoft.com/library/ff393699(v=ws.10).aspx)  `(https://technet.microsoft.com/library/ff393699(v=ws.10).aspx)` for details.</span></span>

```yaml
Type: String
Parameter Sets: RdpPropertyOnly
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c83e-125">-Leírás</span><span class="sxs-lookup"><span data-stu-id="3c83e-125">-Description</span></span>
<span data-ttu-id="3c83e-126">A gyűjtemény rövid leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="3c83e-126">Specifies a short description for the collection.</span></span>

```yaml
Type: String
Parameter Sets: DescriptionOnly
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c83e-127">-Terv</span><span class="sxs-lookup"><span data-stu-id="3c83e-127">-Plan</span></span>
<span data-ttu-id="3c83e-128">Az Azure RemoteApp-gyűjtemény csomagját adja meg, amely meghatározza a használati korlátozásokat.</span><span class="sxs-lookup"><span data-stu-id="3c83e-128">Specifies the plan for the Azure RemoteApp collection, which defines the usage limits.</span></span>
<span data-ttu-id="3c83e-129">Az elérhető csomagok megtekintéséhez használja a **Get-AzureRemoteAppPlan** .</span><span class="sxs-lookup"><span data-stu-id="3c83e-129">Use **Get-AzureRemoteAppPlan** to see the plans available.</span></span>

```yaml
Type: String
Parameter Sets: PlanOnly
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c83e-130">-Profil</span><span class="sxs-lookup"><span data-stu-id="3c83e-130">-Profile</span></span>
<span data-ttu-id="3c83e-131">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="3c83e-131">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3c83e-132">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="3c83e-132">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3c83e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c83e-133">CommonParameters</span></span>
<span data-ttu-id="3c83e-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3c83e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c83e-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c83e-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c83e-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3c83e-136">INPUTS</span></span>

## <span data-ttu-id="3c83e-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3c83e-137">OUTPUTS</span></span>

## <span data-ttu-id="3c83e-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3c83e-138">NOTES</span></span>

## <span data-ttu-id="3c83e-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3c83e-139">RELATED LINKS</span></span>

[<span data-ttu-id="3c83e-140">Get-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="3c83e-140">Get-AzureRemoteAppCollection</span></span>](./Get-AzureRemoteAppCollection.md)

[<span data-ttu-id="3c83e-141">Új – AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="3c83e-141">New-AzureRemoteAppCollection</span></span>](./New-AzureRemoteAppCollection.md)

[<span data-ttu-id="3c83e-142">Update-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="3c83e-142">Update-AzureRemoteAppCollection</span></span>](./Update-AzureRemoteAppCollection.md)


