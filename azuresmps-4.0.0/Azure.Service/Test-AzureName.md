---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 0DF54C9D-7A19-4591-A1FC-33C6A4C9BF33
online version: ''
schema: 2.0.0
ms.openlocfilehash: 05a99e1a4965329c0eeb29fe0e014814fd1807b2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015937"
---
# <span data-ttu-id="9d769-101">Test-AzureName</span><span class="sxs-lookup"><span data-stu-id="9d769-101">Test-AzureName</span></span>

## <span data-ttu-id="9d769-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9d769-102">SYNOPSIS</span></span>
<span data-ttu-id="9d769-103">Annak vizsgálata, hogy a Microsoft Azure Cloud szolgáltatás neve, tárolási szolgáltatás neve vagy a szolgáltatás busza névtér neve létezik-e vagy sem.</span><span class="sxs-lookup"><span data-stu-id="9d769-103">Tests whether a Microsoft Azure cloud service name, storage service name or service bus namespace name exists or not.</span></span>

## <span data-ttu-id="9d769-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9d769-104">SYNTAX</span></span>

### <span data-ttu-id="9d769-105">Szolgáltatás</span><span class="sxs-lookup"><span data-stu-id="9d769-105">Service</span></span>
```
Test-AzureName [-Service] -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="9d769-106">Tárterület</span><span class="sxs-lookup"><span data-stu-id="9d769-106">Storage</span></span>
```
Test-AzureName [-Storage] -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="9d769-107">ServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="9d769-107">ServiceBusNamespace</span></span>
```
Test-AzureName [-ServiceBusNamespace] -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="9d769-108">Webhely</span><span class="sxs-lookup"><span data-stu-id="9d769-108">Website</span></span>
```
Test-AzureName [-Website] -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="9d769-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="9d769-109">DESCRIPTION</span></span>
<span data-ttu-id="9d769-110">Ha a név létezik, a parancsmag $Truet ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="9d769-110">If the name exists, the cmdlet returns $True.</span></span>
<span data-ttu-id="9d769-111">Ha a név nem létezik, akkor az a $False értéket adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="9d769-111">If the name does not exist, it returns $False.</span></span>

## <span data-ttu-id="9d769-112">Példák</span><span class="sxs-lookup"><span data-stu-id="9d769-112">EXAMPLES</span></span>

### <span data-ttu-id="9d769-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="9d769-113">Example 1</span></span>
```
PS C:\> Test-AzureName -Service "MyNameService1"
```

<span data-ttu-id="9d769-114">Ez a parancs azt vizsgálja, hogy az "MyNameService1" egy meglévő Microsoft Azure Cloud-szolgáltatás neve-e.</span><span class="sxs-lookup"><span data-stu-id="9d769-114">This command tests to see if the "MyNameService1" is an existing Microsoft Azure cloud service name.</span></span>

### <span data-ttu-id="9d769-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="9d769-115">Example 2</span></span>
```
PS C:\> Test-AzureName -Storage "mystorename1"
```

<span data-ttu-id="9d769-116">Ez a parancs azt vizsgálja, hogy a "mystorename1" egy meglévő Microsoft Azure Storage Service Name.</span><span class="sxs-lookup"><span data-stu-id="9d769-116">This command tests to see if the "mystorename1" is an existing Microsoft Azure storage service name.</span></span>

### <span data-ttu-id="9d769-117">3. példa</span><span class="sxs-lookup"><span data-stu-id="9d769-117">Example 3</span></span>
```
PS C:\> Test-AzureName -ServiceBusNamespace "mynamespace"
```

<span data-ttu-id="9d769-118">Ez a parancs azt vizsgálja, hogy az "mynamespace" egy meglévő Microsoft Azure Service Bus névtér-név.</span><span class="sxs-lookup"><span data-stu-id="9d769-118">This command tests to see if the "mynamespace" is an existing Microsoft Azure service bus namespace name.</span></span>

## <span data-ttu-id="9d769-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9d769-119">PARAMETERS</span></span>

### <span data-ttu-id="9d769-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9d769-120">-Name</span></span>
<span data-ttu-id="9d769-121">A tesztelni kívánt szolgáltatás vagy tárolási fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9d769-121">Specifies the name of the service or storage account to test.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d769-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="9d769-122">-Profile</span></span>
<span data-ttu-id="9d769-123">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="9d769-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9d769-124">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="9d769-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9d769-125">-Szolgáltatás</span><span class="sxs-lookup"><span data-stu-id="9d769-125">-Service</span></span>
<span data-ttu-id="9d769-126">A meglévő szolgáltatásfiók tesztelését adja meg.</span><span class="sxs-lookup"><span data-stu-id="9d769-126">Specifies to test for an existing service account.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Service
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d769-127">-ServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="9d769-127">-ServiceBusNamespace</span></span>
<span data-ttu-id="9d769-128">Itt határozhatja meg, hogy egy meglévő szolgáltatási busz névteret szeretne-e tesztelni.</span><span class="sxs-lookup"><span data-stu-id="9d769-128">Specifies to test for an existing service bus namespace.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ServiceBusNamespace
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d769-129">-Tárterület</span><span class="sxs-lookup"><span data-stu-id="9d769-129">-Storage</span></span>
<span data-ttu-id="9d769-130">A meglévő tárterület-fiók tesztelését adja meg.</span><span class="sxs-lookup"><span data-stu-id="9d769-130">Specifies to test for an existing storage account.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Storage
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d769-131">-Webhely</span><span class="sxs-lookup"><span data-stu-id="9d769-131">-Website</span></span>
<span data-ttu-id="9d769-132">A meglévő webhelyek tesztelését adja meg.</span><span class="sxs-lookup"><span data-stu-id="9d769-132">Specifies to test for an existing website.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Website
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d769-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d769-133">CommonParameters</span></span>
<span data-ttu-id="9d769-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9d769-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d769-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d769-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d769-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9d769-136">INPUTS</span></span>

## <span data-ttu-id="9d769-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9d769-137">OUTPUTS</span></span>

## <span data-ttu-id="9d769-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9d769-138">NOTES</span></span>
* <span data-ttu-id="9d769-139">Node-dev, php-dev, Python-dev</span><span class="sxs-lookup"><span data-stu-id="9d769-139">node-dev, php-dev, python-dev</span></span>

## <span data-ttu-id="9d769-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9d769-140">RELATED LINKS</span></span>

