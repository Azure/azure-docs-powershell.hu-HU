---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: CF429CF0-2AB2-4E31-8A0D-AE5C8D77A76B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0d1ad08d88cb5b89b0537b19f8ea4aaef0000cbb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015607"
---
# <span data-ttu-id="5ca7a-101">Get-AzureServiceADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="5ca7a-101">Get-AzureServiceADDomainExtension</span></span>

## <span data-ttu-id="5ca7a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5ca7a-102">SYNOPSIS</span></span>
<span data-ttu-id="5ca7a-103">A felhőalapú szolgáltatás Active Directory (AD) tartományi bővítményét adja meg, amely az összes szerepkörre vagy az elnevezett szerepkörökre vonatkozik egy adott központi üzembe helyezési bővítőhelyen.</span><span class="sxs-lookup"><span data-stu-id="5ca7a-103">Gets the cloud service Active Directory (AD) domain extension that applies to all roles or to named roles at a specified deployment slot.</span></span>

## <span data-ttu-id="5ca7a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5ca7a-104">SYNTAX</span></span>

```
Get-AzureServiceADDomainExtension [[-ServiceName] <String>] [[-Slot] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="5ca7a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5ca7a-105">DESCRIPTION</span></span>
<span data-ttu-id="5ca7a-106">A **Get-AzureServiceADDomainExtension** parancsmag a FELHŐALAPÚ szolgáltatás ad tartományi bővítményét adja meg, amely egy adott központi üzembe helyezési bővítőhely minden szerepkörére vagy elnevezett szerepkörére érvényes.</span><span class="sxs-lookup"><span data-stu-id="5ca7a-106">The **Get-AzureServiceADDomainExtension** cmdlet gets the cloud service AD domain extension that applies to all roles or named roles at a specified deployment slot.</span></span>

## <span data-ttu-id="5ca7a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="5ca7a-107">EXAMPLES</span></span>

### <span data-ttu-id="5ca7a-108">Példa 1: adott szolgáltatáshoz tartozó AD domain-bővítmény beszerzése</span><span class="sxs-lookup"><span data-stu-id="5ca7a-108">Example 1: Get the AD domain extension for a specified service</span></span>
```
PS C:\> Get-AzureServiceADDomainExtension -ServiceName $Svc
```

<span data-ttu-id="5ca7a-109">Ez a parancs a $Svcban megadott szolgáltatás AD domain bővítményét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="5ca7a-109">This command gets the AD domain extension for the service specified in $Svc.</span></span>

## <span data-ttu-id="5ca7a-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5ca7a-110">PARAMETERS</span></span>

### <span data-ttu-id="5ca7a-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="5ca7a-111">-InformationAction</span></span>
<span data-ttu-id="5ca7a-112">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="5ca7a-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="5ca7a-113">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="5ca7a-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5ca7a-114">Folytassa</span><span class="sxs-lookup"><span data-stu-id="5ca7a-114">Continue</span></span>
- <span data-ttu-id="5ca7a-115">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="5ca7a-115">Ignore</span></span>
- <span data-ttu-id="5ca7a-116">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="5ca7a-116">Inquire</span></span>
- <span data-ttu-id="5ca7a-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="5ca7a-117">SilentlyContinue</span></span>
- <span data-ttu-id="5ca7a-118">állj</span><span class="sxs-lookup"><span data-stu-id="5ca7a-118">Stop</span></span>
- <span data-ttu-id="5ca7a-119">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="5ca7a-119">Suspend</span></span>

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

### <span data-ttu-id="5ca7a-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="5ca7a-120">-InformationVariable</span></span>
<span data-ttu-id="5ca7a-121">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="5ca7a-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="5ca7a-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="5ca7a-122">-Profile</span></span>
<span data-ttu-id="5ca7a-123">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="5ca7a-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5ca7a-124">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="5ca7a-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5ca7a-125">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="5ca7a-125">-ServiceName</span></span>
<span data-ttu-id="5ca7a-126">A központi üzembe helyezés Azure-szolgáltatás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5ca7a-126">Specifies the Azure service name of the deployment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ca7a-127">-Slot</span><span class="sxs-lookup"><span data-stu-id="5ca7a-127">-Slot</span></span>
<span data-ttu-id="5ca7a-128">A központi telepítő környezetet adja meg.</span><span class="sxs-lookup"><span data-stu-id="5ca7a-128">Specifies the deployment environment.</span></span>
<span data-ttu-id="5ca7a-129">A paraméter elfogadható értékei a következők: termelés vagy megállóhely.</span><span class="sxs-lookup"><span data-stu-id="5ca7a-129">The acceptable values for this parameter are: Production or Staging.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ca7a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ca7a-130">CommonParameters</span></span>
<span data-ttu-id="5ca7a-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5ca7a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ca7a-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ca7a-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ca7a-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5ca7a-133">INPUTS</span></span>

## <span data-ttu-id="5ca7a-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5ca7a-134">OUTPUTS</span></span>

## <span data-ttu-id="5ca7a-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5ca7a-135">NOTES</span></span>

## <span data-ttu-id="5ca7a-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5ca7a-136">RELATED LINKS</span></span>

[<span data-ttu-id="5ca7a-137">Remove-AzureServiceADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="5ca7a-137">Remove-AzureServiceADDomainExtension</span></span>](./Remove-AzureServiceADDomainExtension.md)

[<span data-ttu-id="5ca7a-138">Set-AzureServiceADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="5ca7a-138">Set-AzureServiceADDomainExtension</span></span>](./Set-AzureServiceADDomainExtension.md)


