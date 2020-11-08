---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 4A920D84-0005-45A2-8229-FD9436A2CA6D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 927520466299776326229976b355444f9db6c23e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016049"
---
# <span data-ttu-id="c39f8-101">Set-AzureService</span><span class="sxs-lookup"><span data-stu-id="c39f8-101">Set-AzureService</span></span>

## <span data-ttu-id="c39f8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c39f8-102">SYNOPSIS</span></span>
<span data-ttu-id="c39f8-103">Beállítja vagy frissíti a megadott Microsoft Azure-szolgáltatás címkéjét és leírását.</span><span class="sxs-lookup"><span data-stu-id="c39f8-103">Sets or updates the label and description of the specified Microsoft Azure service.</span></span>

## <span data-ttu-id="c39f8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c39f8-104">SYNTAX</span></span>

```
Set-AzureService [-ServiceName] <String> [[-Label] <String>] [[-Description] <String>]
 [[-ReverseDnsFqdn] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="c39f8-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c39f8-105">DESCRIPTION</span></span>
<span data-ttu-id="c39f8-106">A **set-AzureService** parancsmag címkét és leírást rendel a szolgáltatáshoz az aktuális előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="c39f8-106">The **Set-AzureService** cmdlet assigns a label and description to a service in the current subscription.</span></span>

## <span data-ttu-id="c39f8-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c39f8-107">EXAMPLES</span></span>

### <span data-ttu-id="c39f8-108">Példa 1: a szolgáltatás címkéjének és leírásának frissítése</span><span class="sxs-lookup"><span data-stu-id="c39f8-108">Example 1: Update the label and description for a service</span></span>
```
PS C:\> C:\PS>Set-AzureService -ServiceName "MySvc1" -Label "MyTestSvc1" -Description "My service for testing out new configurations"
```

<span data-ttu-id="c39f8-109">Ez a parancs beállítja a címkét "MyTestSvc1", valamint a "saját szolgáltatás az új konfigurációk kipróbálására" leírást a MyTestSvc1 szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="c39f8-109">This command sets the label to "MyTestSvc1" and the description to "My service for testing out new configurations" for the MyTestSvc1 service.</span></span>

## <span data-ttu-id="c39f8-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c39f8-110">PARAMETERS</span></span>

### <span data-ttu-id="c39f8-111">-Leírás</span><span class="sxs-lookup"><span data-stu-id="c39f8-111">-Description</span></span>
<span data-ttu-id="c39f8-112">Az Azure szolgáltatás leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="c39f8-112">Specifies a description for the Azure service.</span></span>
<span data-ttu-id="c39f8-113">A Leírás legfeljebb 1024 karakter hosszú lehet.</span><span class="sxs-lookup"><span data-stu-id="c39f8-113">The description may be up to 1024 characters in length.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c39f8-114">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="c39f8-114">-InformationAction</span></span>
<span data-ttu-id="c39f8-115">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="c39f8-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="c39f8-116">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="c39f8-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c39f8-117">Folytassa</span><span class="sxs-lookup"><span data-stu-id="c39f8-117">Continue</span></span>
- <span data-ttu-id="c39f8-118">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="c39f8-118">Ignore</span></span>
- <span data-ttu-id="c39f8-119">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="c39f8-119">Inquire</span></span>
- <span data-ttu-id="c39f8-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="c39f8-120">SilentlyContinue</span></span>
- <span data-ttu-id="c39f8-121">állj</span><span class="sxs-lookup"><span data-stu-id="c39f8-121">Stop</span></span>
- <span data-ttu-id="c39f8-122">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="c39f8-122">Suspend</span></span>

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

### <span data-ttu-id="c39f8-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="c39f8-123">-InformationVariable</span></span>
<span data-ttu-id="c39f8-124">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="c39f8-124">Specifies an information variable.</span></span>

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

### <span data-ttu-id="c39f8-125">-Label (címke)</span><span class="sxs-lookup"><span data-stu-id="c39f8-125">-Label</span></span>
<span data-ttu-id="c39f8-126">Az Azure szolgáltatás címkét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c39f8-126">Specifies a label for the Azure service.</span></span>
<span data-ttu-id="c39f8-127">Előfordulhat, hogy a címke hossza legfeljebb 100 karakter lehet.</span><span class="sxs-lookup"><span data-stu-id="c39f8-127">The label may be up to 100 characters in length.</span></span>

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

### <span data-ttu-id="c39f8-128">-Profil</span><span class="sxs-lookup"><span data-stu-id="c39f8-128">-Profile</span></span>
<span data-ttu-id="c39f8-129">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="c39f8-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c39f8-130">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="c39f8-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c39f8-131">-ReverseDnsFqdn</span><span class="sxs-lookup"><span data-stu-id="c39f8-131">-ReverseDnsFqdn</span></span>
<span data-ttu-id="c39f8-132">A DNS-név teljes tartománynevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c39f8-132">Specifies the fully qualified domain name for reverse DNS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c39f8-133">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="c39f8-133">-ServiceName</span></span>
<span data-ttu-id="c39f8-134">A frissítendő Azure-szolgáltatás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c39f8-134">Specifies the name of the Azure service to update.</span></span>

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

### <span data-ttu-id="c39f8-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c39f8-135">CommonParameters</span></span>
<span data-ttu-id="c39f8-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c39f8-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c39f8-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c39f8-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c39f8-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c39f8-138">INPUTS</span></span>

## <span data-ttu-id="c39f8-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c39f8-139">OUTPUTS</span></span>

### <span data-ttu-id="c39f8-140">ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="c39f8-140">ManagementOperationContext</span></span>

## <span data-ttu-id="c39f8-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c39f8-141">NOTES</span></span>

## <span data-ttu-id="c39f8-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c39f8-142">RELATED LINKS</span></span>

[<span data-ttu-id="c39f8-143">Get-AzureService</span><span class="sxs-lookup"><span data-stu-id="c39f8-143">Get-AzureService</span></span>](./Get-AzureService.md)

[<span data-ttu-id="c39f8-144">Új – AzureService</span><span class="sxs-lookup"><span data-stu-id="c39f8-144">New-AzureService</span></span>](./New-AzureService.md)


