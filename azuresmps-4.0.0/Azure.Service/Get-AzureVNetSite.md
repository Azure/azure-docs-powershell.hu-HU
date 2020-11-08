---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: CFAA371E-F320-4FC3-80E0-5C857E5C0998
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0fbb80550acb0c743a3134a315f790bc25fb793a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016527"
---
# <span data-ttu-id="30ec3-101">Get-AzureVNetSite</span><span class="sxs-lookup"><span data-stu-id="30ec3-101">Get-AzureVNetSite</span></span>

## <span data-ttu-id="30ec3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="30ec3-102">SYNOPSIS</span></span>
<span data-ttu-id="30ec3-103">A List objektum lekérdezése az Azure virtuális hálózatokkal kapcsolatos információkat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="30ec3-103">Gets a list object with information about Azure virtual networks.</span></span>

## <span data-ttu-id="30ec3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="30ec3-104">SYNTAX</span></span>

```
Get-AzureVNetSite [[-VNetName] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="30ec3-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="30ec3-105">DESCRIPTION</span></span>
<span data-ttu-id="30ec3-106">A **Get-AzureVNetSite** parancsmag olyan lista-objektumot kap, amely az aktuális előfizetéshez tartozó Azure virtuális hálózatokra vonatkozó információkat tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="30ec3-106">The **Get-AzureVNetSite** cmdlet gets a list object with information about Azure virtual networks for the current subscription.</span></span>
<span data-ttu-id="30ec3-107">Ha megad egy virtuális hálózat nevét, akkor csak az adott virtuális hálózatra vonatkozó információk jelennek meg.</span><span class="sxs-lookup"><span data-stu-id="30ec3-107">If you specify a virtual network name, only information for that virtual network is returned.</span></span>

## <span data-ttu-id="30ec3-108">Példák</span><span class="sxs-lookup"><span data-stu-id="30ec3-108">EXAMPLES</span></span>

### <span data-ttu-id="30ec3-109">1. példa: információk kérése az aktuális előfizetéshez tartozó összes virtuális hálózatról</span><span class="sxs-lookup"><span data-stu-id="30ec3-109">Example 1: Get information about all virtual networks in the current subscription</span></span>
```
PS C:\> Get-AzureVNetSite
```

<span data-ttu-id="30ec3-110">Ez a parancs a jelenlegi előfizetésben lévő összes virtuális hálózatról információt kap.</span><span class="sxs-lookup"><span data-stu-id="30ec3-110">This command gets information about all the virtual networks in the current subscription.</span></span>

### <span data-ttu-id="30ec3-111">2. példa: információk kérése egy adott virtuális hálózatról az aktuális előfizetésben</span><span class="sxs-lookup"><span data-stu-id="30ec3-111">Example 2: Get information about a specific virtual network in the current subscription</span></span>
```
PS C:\> Get-AzureVNetSite -VNetName "MyProductionNetwork"
```

<span data-ttu-id="30ec3-112">Ez a parancs csak a MyProductionNetwork virtuális hálózatra keres információkat.</span><span class="sxs-lookup"><span data-stu-id="30ec3-112">This command retrieves information on the MyProductionNetwork virtual network only.</span></span>

## <span data-ttu-id="30ec3-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="30ec3-113">PARAMETERS</span></span>

### <span data-ttu-id="30ec3-114">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="30ec3-114">-InformationAction</span></span>
<span data-ttu-id="30ec3-115">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="30ec3-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="30ec3-116">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="30ec3-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="30ec3-117">Folytassa</span><span class="sxs-lookup"><span data-stu-id="30ec3-117">Continue</span></span>
- <span data-ttu-id="30ec3-118">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="30ec3-118">Ignore</span></span>
- <span data-ttu-id="30ec3-119">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="30ec3-119">Inquire</span></span>
- <span data-ttu-id="30ec3-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="30ec3-120">SilentlyContinue</span></span>
- <span data-ttu-id="30ec3-121">állj</span><span class="sxs-lookup"><span data-stu-id="30ec3-121">Stop</span></span>
- <span data-ttu-id="30ec3-122">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="30ec3-122">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30ec3-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="30ec3-123">-InformationVariable</span></span>
<span data-ttu-id="30ec3-124">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="30ec3-124">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30ec3-125">-Profil</span><span class="sxs-lookup"><span data-stu-id="30ec3-125">-Profile</span></span>
<span data-ttu-id="30ec3-126">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="30ec3-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="30ec3-127">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="30ec3-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="30ec3-128">-VNetName</span><span class="sxs-lookup"><span data-stu-id="30ec3-128">-VNetName</span></span>
<span data-ttu-id="30ec3-129">Megadja a virtuális hálózati nevet, amellyel információt ad vissza.</span><span class="sxs-lookup"><span data-stu-id="30ec3-129">Specifies a virtual network name to return information about.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30ec3-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30ec3-130">CommonParameters</span></span>
<span data-ttu-id="30ec3-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="30ec3-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30ec3-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30ec3-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30ec3-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="30ec3-133">INPUTS</span></span>

## <span data-ttu-id="30ec3-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="30ec3-134">OUTPUTS</span></span>

## <span data-ttu-id="30ec3-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="30ec3-135">NOTES</span></span>

## <span data-ttu-id="30ec3-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="30ec3-136">RELATED LINKS</span></span>

[<span data-ttu-id="30ec3-137">Get-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="30ec3-137">Get-AzureVNetConfig</span></span>](./Get-AzureVNetConfig.md)

[<span data-ttu-id="30ec3-138">Remove-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="30ec3-138">Remove-AzureVNetConfig</span></span>](./Remove-AzureVNetConfig.md)

[<span data-ttu-id="30ec3-139">Set-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="30ec3-139">Set-AzureVNetConfig</span></span>](./Set-AzureVNetConfig.md)


