---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 3F3BC5AF-8D7B-40BF-A072-A11C7BDCB6B3
online version: ''
schema: 2.0.0
ms.openlocfilehash: 09adc7e9b2faf9b9a905fa1c94fb6526e02c110f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015786"
---
# <span data-ttu-id="55c8a-101">Set-AzureWalkUpgradeDomain</span><span class="sxs-lookup"><span data-stu-id="55c8a-101">Set-AzureWalkUpgradeDomain</span></span>

## <span data-ttu-id="55c8a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="55c8a-102">SYNOPSIS</span></span>
<span data-ttu-id="55c8a-103">A megadott frissítési tartomány besétálása</span><span class="sxs-lookup"><span data-stu-id="55c8a-103">Walks the specified upgrade domain.</span></span>

## <span data-ttu-id="55c8a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="55c8a-104">SYNTAX</span></span>

```
Set-AzureWalkUpgradeDomain [-ServiceName] <String> [-Slot] <String> [-DomainNumber] <Int32>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="55c8a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="55c8a-105">DESCRIPTION</span></span>
<span data-ttu-id="55c8a-106">A **set-AzureWalkUpgradeDomain** parancsmag az Azure-példány tényleges frissítését kezdeményezi.</span><span class="sxs-lookup"><span data-stu-id="55c8a-106">The **Set-AzureWalkUpgradeDomain** cmdlet initiates the actual upgrade of an Azure deployment.</span></span>
<span data-ttu-id="55c8a-107">A frissítési csomagot és a konfigurációt a **set-AzureDeployment** parancsmag és a-upgrade kapcsoló használatával állíthatja be.</span><span class="sxs-lookup"><span data-stu-id="55c8a-107">The upgrade package and configuration are set by using the **Set-AzureDeployment** cmdlet with the -Upgrade switch.</span></span>

## <span data-ttu-id="55c8a-108">Példák</span><span class="sxs-lookup"><span data-stu-id="55c8a-108">EXAMPLES</span></span>

### <span data-ttu-id="55c8a-109">Példa 1: a termelési példány frissítésének kezdeményezése</span><span class="sxs-lookup"><span data-stu-id="55c8a-109">Example 1: Initiate an upgrade of a production deployment</span></span>
```
PS C:\> Set-AzureWalkUpgradeDomain -ServiceName "MySvc1" -slot "Production" -UpgradeDomain 2
```

<span data-ttu-id="55c8a-110">Ez a parancs elindítja az upgrade (2. tartomány) frissítését a MySvc1 szolgáltatás termelésének központi verziójában.</span><span class="sxs-lookup"><span data-stu-id="55c8a-110">This command initiates the upgrade of Upgrade Domain 2 of the production deployment of the MySvc1 service.</span></span>

## <span data-ttu-id="55c8a-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="55c8a-111">PARAMETERS</span></span>

### <span data-ttu-id="55c8a-112">-DomainNumber</span><span class="sxs-lookup"><span data-stu-id="55c8a-112">-DomainNumber</span></span>
<span data-ttu-id="55c8a-113">A frissítendő tartományt adja meg.</span><span class="sxs-lookup"><span data-stu-id="55c8a-113">Specifies the upgrade domain to upgrade.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55c8a-114">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="55c8a-114">-InformationAction</span></span>
<span data-ttu-id="55c8a-115">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="55c8a-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="55c8a-116">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="55c8a-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="55c8a-117">Folytassa</span><span class="sxs-lookup"><span data-stu-id="55c8a-117">Continue</span></span>
- <span data-ttu-id="55c8a-118">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="55c8a-118">Ignore</span></span>
- <span data-ttu-id="55c8a-119">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="55c8a-119">Inquire</span></span>
- <span data-ttu-id="55c8a-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="55c8a-120">SilentlyContinue</span></span>
- <span data-ttu-id="55c8a-121">állj</span><span class="sxs-lookup"><span data-stu-id="55c8a-121">Stop</span></span>
- <span data-ttu-id="55c8a-122">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="55c8a-122">Suspend</span></span>

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

### <span data-ttu-id="55c8a-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="55c8a-123">-InformationVariable</span></span>
<span data-ttu-id="55c8a-124">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="55c8a-124">Specifies an information variable.</span></span>

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

### <span data-ttu-id="55c8a-125">-Profil</span><span class="sxs-lookup"><span data-stu-id="55c8a-125">-Profile</span></span>
<span data-ttu-id="55c8a-126">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="55c8a-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="55c8a-127">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="55c8a-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="55c8a-128">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="55c8a-128">-ServiceName</span></span>
<span data-ttu-id="55c8a-129">A frissítendő Microsoft Azure-szolgáltatás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="55c8a-129">Specifies the Microsoft Azure service name to upgrade.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55c8a-130">-Slot</span><span class="sxs-lookup"><span data-stu-id="55c8a-130">-Slot</span></span>
<span data-ttu-id="55c8a-131">A frissítendő központi verzió környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="55c8a-131">Specifies the environment of the deployment to upgrade.</span></span>

<span data-ttu-id="55c8a-132">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="55c8a-132">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="55c8a-133">Átmeneti tárolásra szolgáló</span><span class="sxs-lookup"><span data-stu-id="55c8a-133">Staging</span></span>
- <span data-ttu-id="55c8a-134">Production</span><span class="sxs-lookup"><span data-stu-id="55c8a-134">Production</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55c8a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55c8a-135">CommonParameters</span></span>
<span data-ttu-id="55c8a-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="55c8a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55c8a-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55c8a-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55c8a-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="55c8a-138">INPUTS</span></span>

## <span data-ttu-id="55c8a-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="55c8a-139">OUTPUTS</span></span>

### <span data-ttu-id="55c8a-140">ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="55c8a-140">ManagementOperationContext</span></span>

## <span data-ttu-id="55c8a-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="55c8a-141">NOTES</span></span>

## <span data-ttu-id="55c8a-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="55c8a-142">RELATED LINKS</span></span>

[<span data-ttu-id="55c8a-143">Set-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="55c8a-143">Set-AzureDeployment</span></span>](./Set-AzureDeployment.md)


