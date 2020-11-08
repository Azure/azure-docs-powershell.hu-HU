---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 5BEE9430-D6BF-49F1-A23D-32784C6C818E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 98b9abe6bcb9998067fe978a5f99f5d8b64cd26d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016331"
---
# <span data-ttu-id="f995b-101">Get-AzurePublicIP</span><span class="sxs-lookup"><span data-stu-id="f995b-101">Get-AzurePublicIP</span></span>

## <span data-ttu-id="f995b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f995b-102">SYNOPSIS</span></span>
<span data-ttu-id="f995b-103">Az Azure Virtual Machine nyilvános IP-információit kapja.</span><span class="sxs-lookup"><span data-stu-id="f995b-103">Gets the Public IP information for an Azure virtual machine.</span></span>

## <span data-ttu-id="f995b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f995b-104">SYNTAX</span></span>

```
Get-AzurePublicIP [[-PublicIPName] <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="f995b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f995b-105">DESCRIPTION</span></span>
<span data-ttu-id="f995b-106">A **Get-AzurePublicIP** parancsmag az Azure Virtual Machine nyilvános IP-adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="f995b-106">The **Get-AzurePublicIP** cmdlet gets the Public IP information for an Azure virtual machine.</span></span>
<span data-ttu-id="f995b-107">A nyilvános IP-cím IP-címének beszerzéséhez használja a **Get-AzureVM** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="f995b-107">To obtain the IP address of the Public IP, use the **Get-AzureVM** cmdlet.</span></span>

## <span data-ttu-id="f995b-108">Példák</span><span class="sxs-lookup"><span data-stu-id="f995b-108">EXAMPLES</span></span>

### <span data-ttu-id="f995b-109">Példa 1: nyilvános IP-konfiguráció beszerzése</span><span class="sxs-lookup"><span data-stu-id="f995b-109">Example 1: Get Public IP configuration</span></span>
```
PS C:\> Get-AzureVM -ServiceName "FTPInAzure" -Name "FTPInstance" | Get-AzurePublicIP
```

<span data-ttu-id="f995b-110">Ez a parancs a **Get-AzureVM** parancsmag használatával kapja meg a FTPInstance nevű virtuális gépet a FTPInAzure nevű szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="f995b-110">This command gets the virtual machine named FTPInstance in the service named FTPInAzure by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="f995b-111">A parancs a virtuális gépet az aktuális parancsmagra átadja a pipeline operátor használatával.</span><span class="sxs-lookup"><span data-stu-id="f995b-111">The command passes that virtual machine to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="f995b-112">Az aktuális parancsmag a virtuális gép nyilvános IP-konfigurációját kapja.</span><span class="sxs-lookup"><span data-stu-id="f995b-112">The current cmdlet gets Public IP configuration from the virtual machine.</span></span>

## <span data-ttu-id="f995b-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f995b-113">PARAMETERS</span></span>

### <span data-ttu-id="f995b-114">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="f995b-114">-InformationAction</span></span>
<span data-ttu-id="f995b-115">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="f995b-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="f995b-116">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="f995b-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f995b-117">Folytassa</span><span class="sxs-lookup"><span data-stu-id="f995b-117">Continue</span></span>
- <span data-ttu-id="f995b-118">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="f995b-118">Ignore</span></span>
- <span data-ttu-id="f995b-119">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="f995b-119">Inquire</span></span>
- <span data-ttu-id="f995b-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="f995b-120">SilentlyContinue</span></span>
- <span data-ttu-id="f995b-121">állj</span><span class="sxs-lookup"><span data-stu-id="f995b-121">Stop</span></span>
- <span data-ttu-id="f995b-122">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="f995b-122">Suspend</span></span>

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

### <span data-ttu-id="f995b-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="f995b-123">-InformationVariable</span></span>
<span data-ttu-id="f995b-124">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="f995b-124">Specifies an information variable.</span></span>

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

### <span data-ttu-id="f995b-125">-Profil</span><span class="sxs-lookup"><span data-stu-id="f995b-125">-Profile</span></span>
<span data-ttu-id="f995b-126">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="f995b-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f995b-127">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="f995b-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f995b-128">-PublicIPName</span><span class="sxs-lookup"><span data-stu-id="f995b-128">-PublicIPName</span></span>
<span data-ttu-id="f995b-129">Adja meg a nyilvános IP-nevet.</span><span class="sxs-lookup"><span data-stu-id="f995b-129">Specifies the Public IP name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f995b-130">-VM</span><span class="sxs-lookup"><span data-stu-id="f995b-130">-VM</span></span>
<span data-ttu-id="f995b-131">Azt a virtuális gépet adja meg, amelynek a parancsmagja nyilvános IP-konfigurációt kap.</span><span class="sxs-lookup"><span data-stu-id="f995b-131">Specifies the virtual machine for which this cmdlet gets Public IP configuration.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f995b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f995b-132">CommonParameters</span></span>
<span data-ttu-id="f995b-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f995b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f995b-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f995b-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f995b-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f995b-135">INPUTS</span></span>

## <span data-ttu-id="f995b-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f995b-136">OUTPUTS</span></span>

### <span data-ttu-id="f995b-137">Microsoft. WindowsAzure. Command. ServiceManagement. AssignPublicIPCollection</span><span class="sxs-lookup"><span data-stu-id="f995b-137">Microsoft.WindowsAzure.Commands.ServiceManagement.AssignPublicIPCollection</span></span>

## <span data-ttu-id="f995b-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f995b-138">NOTES</span></span>

## <span data-ttu-id="f995b-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f995b-139">RELATED LINKS</span></span>

[<span data-ttu-id="f995b-140">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="f995b-140">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="f995b-141">Remove-AzurePublicIP</span><span class="sxs-lookup"><span data-stu-id="f995b-141">Remove-AzurePublicIP</span></span>](./Remove-AzurePublicIP.md)

[<span data-ttu-id="f995b-142">Set-AzurePublicIP</span><span class="sxs-lookup"><span data-stu-id="f995b-142">Set-AzurePublicIP</span></span>](./Set-AzurePublicIP.md)


