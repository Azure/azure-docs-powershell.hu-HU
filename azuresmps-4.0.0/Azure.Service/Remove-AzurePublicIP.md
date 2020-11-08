---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 9EA98944-1923-4573-991E-3B9CA21004BB
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2f16b51dc8abf5c6243b4b489789d65029acc3c4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016148"
---
# <span data-ttu-id="e96a4-101">Remove-AzurePublicIP</span><span class="sxs-lookup"><span data-stu-id="e96a4-101">Remove-AzurePublicIP</span></span>

## <span data-ttu-id="e96a4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e96a4-102">SYNOPSIS</span></span>
<span data-ttu-id="e96a4-103">Eltávolítja a nyilvános IP-konfigurációt egy Azure Virtual Machine-ből.</span><span class="sxs-lookup"><span data-stu-id="e96a4-103">Removes Public IP configuration from an Azure virtual machine.</span></span>

## <span data-ttu-id="e96a4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e96a4-104">SYNTAX</span></span>

```
Remove-AzurePublicIP [[-PublicIPName] <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="e96a4-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e96a4-105">DESCRIPTION</span></span>
<span data-ttu-id="e96a4-106">A **Remove-AzurePublicIP** parancsmag eltávolítja a nyilvános IP-konfigurációt egy Azure Virtual Machine-webhelyről.</span><span class="sxs-lookup"><span data-stu-id="e96a4-106">The **Remove-AzurePublicIP** cmdlet removes Public IP configuration from an Azure virtual machine.</span></span>

## <span data-ttu-id="e96a4-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e96a4-107">EXAMPLES</span></span>

### <span data-ttu-id="e96a4-108">1. példa: nyilvános IP-konfiguráció eltávolítása</span><span class="sxs-lookup"><span data-stu-id="e96a4-108">Example 1: Remove Public IP configuration</span></span>
```
PS C:\> Get-AzureVM -ServiceName "FTPInAzure" -Name "FTPInstance" | Remove-AzurePublicIP | Update-AzureVM
```

<span data-ttu-id="e96a4-109">Ez a parancs a **Get-AzureVM** parancsmag használatával kapja meg a FTPInstance nevű virtuális gépet a FTPInAzure nevű szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="e96a4-109">This command gets the virtual machine named FTPInstance in the service named FTPInAzure by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="e96a4-110">A parancs a virtuális gépet az aktuális parancsmagra átadja a pipeline operátor használatával.</span><span class="sxs-lookup"><span data-stu-id="e96a4-110">The command passes that virtual machine to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="e96a4-111">Az aktuális parancsmag eltávolítja a nyilvános IP-konfigurációt a virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="e96a4-111">The current cmdlet removes Public IP configuration from the virtual machine.</span></span>
<span data-ttu-id="e96a4-112">A parancs átadja a virtuális gépet az **Update-AzureVM** parancsmagnak, amely végrehajtja a módosításokat.</span><span class="sxs-lookup"><span data-stu-id="e96a4-112">The command passes the virtual machine to the **Update-AzureVM** cmdlet, which implements your changes.</span></span>

## <span data-ttu-id="e96a4-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e96a4-113">PARAMETERS</span></span>

### <span data-ttu-id="e96a4-114">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="e96a4-114">-InformationAction</span></span>
<span data-ttu-id="e96a4-115">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="e96a4-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="e96a4-116">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="e96a4-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e96a4-117">Folytassa</span><span class="sxs-lookup"><span data-stu-id="e96a4-117">Continue</span></span>
- <span data-ttu-id="e96a4-118">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="e96a4-118">Ignore</span></span>
- <span data-ttu-id="e96a4-119">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="e96a4-119">Inquire</span></span>
- <span data-ttu-id="e96a4-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="e96a4-120">SilentlyContinue</span></span>
- <span data-ttu-id="e96a4-121">állj</span><span class="sxs-lookup"><span data-stu-id="e96a4-121">Stop</span></span>
- <span data-ttu-id="e96a4-122">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="e96a4-122">Suspend</span></span>

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

### <span data-ttu-id="e96a4-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="e96a4-123">-InformationVariable</span></span>
<span data-ttu-id="e96a4-124">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="e96a4-124">Specifies an information variable.</span></span>

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

### <span data-ttu-id="e96a4-125">-Profil</span><span class="sxs-lookup"><span data-stu-id="e96a4-125">-Profile</span></span>
<span data-ttu-id="e96a4-126">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="e96a4-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e96a4-127">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="e96a4-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e96a4-128">-PublicIPName</span><span class="sxs-lookup"><span data-stu-id="e96a4-128">-PublicIPName</span></span>
<span data-ttu-id="e96a4-129">Adja meg a nyilvános IP-nevet.</span><span class="sxs-lookup"><span data-stu-id="e96a4-129">Specifies the Public IP name.</span></span>

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

### <span data-ttu-id="e96a4-130">-VM</span><span class="sxs-lookup"><span data-stu-id="e96a4-130">-VM</span></span>
<span data-ttu-id="e96a4-131">Azt a virtuális gépet adja meg, amelyből a parancsmag eltávolítja a nyilvános IP-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="e96a4-131">Specifies the virtual machine from which this cmdlet removes Public IP configuration.</span></span>

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

### <span data-ttu-id="e96a4-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e96a4-132">CommonParameters</span></span>
<span data-ttu-id="e96a4-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e96a4-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e96a4-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e96a4-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e96a4-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e96a4-135">INPUTS</span></span>

## <span data-ttu-id="e96a4-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e96a4-136">OUTPUTS</span></span>

### <span data-ttu-id="e96a4-137">Microsoft. WindowsAzure. Command. ServiceManagement. Model. IPersistentVM</span><span class="sxs-lookup"><span data-stu-id="e96a4-137">Microsoft.WindowsAzure.Commands.ServiceManagement.Model.IPersistentVM</span></span>

## <span data-ttu-id="e96a4-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e96a4-138">NOTES</span></span>

## <span data-ttu-id="e96a4-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e96a4-139">RELATED LINKS</span></span>

[<span data-ttu-id="e96a4-140">Get-AzurePublicIP</span><span class="sxs-lookup"><span data-stu-id="e96a4-140">Get-AzurePublicIP</span></span>](./Get-AzurePublicIP.md)

[<span data-ttu-id="e96a4-141">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="e96a4-141">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="e96a4-142">Set-AzurePublicIP</span><span class="sxs-lookup"><span data-stu-id="e96a4-142">Set-AzurePublicIP</span></span>](./Set-AzurePublicIP.md)

[<span data-ttu-id="e96a4-143">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="e96a4-143">Update-AzureVM</span></span>](./Update-AzureVM.md)


