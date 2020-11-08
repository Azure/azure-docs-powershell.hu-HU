---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 915CBA29-5A58-4A5D-9F02-976CB76D4800
online version: ''
schema: 2.0.0
ms.openlocfilehash: af98cbdc0be73c87682d0ed004d17cd9e82c9baa
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016175"
---
# <span data-ttu-id="f2cdd-101">Remove-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="f2cdd-101">Remove-AzureAclConfig</span></span>

## <span data-ttu-id="f2cdd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f2cdd-102">SYNOPSIS</span></span>
<span data-ttu-id="f2cdd-103">ACL-konfigurációs objektum eltávolítása Azure Virtual Machine-konfigurációból.</span><span class="sxs-lookup"><span data-stu-id="f2cdd-103">Removes an ACL configuration object from an Azure virtual machine configuration.</span></span>

## <span data-ttu-id="f2cdd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f2cdd-104">SYNTAX</span></span>

```
Remove-AzureAclConfig [-EndpointName] <String> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="f2cdd-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f2cdd-105">DESCRIPTION</span></span>
<span data-ttu-id="f2cdd-106">A **Remove-AzureAclConfig** parancsmag eltávolítja a hozzáférés-vezérlési lista (ACL) konfigurációs objektumát egy Azure Virtual Machine-konfigurációból.</span><span class="sxs-lookup"><span data-stu-id="f2cdd-106">The **Remove-AzureAclConfig** cmdlet removes an access control list (ACL) configuration object from an Azure virtual machine configuration.</span></span>

## <span data-ttu-id="f2cdd-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f2cdd-107">EXAMPLES</span></span>

### <span data-ttu-id="f2cdd-108">Példa 1: ACL-konfiguráció eltávolítása</span><span class="sxs-lookup"><span data-stu-id="f2cdd-108">Example 1: Remove an ACL configuration</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Remove-AzureAclConfig -EndpointName "Web" | Update-AzureVM
```

<span data-ttu-id="f2cdd-109">Ez a parancs a **Get-AzureVM** parancsmag használatával kapja meg a VirtualMachine07 nevű virtuális gépet a ContosoService nevű szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="f2cdd-109">This command gets the virtual machine named VirtualMachine07 in the service named ContosoService by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="f2cdd-110">A parancs a csővezeték-kezelő használatával továbbítja az objektumot az aktuális parancsmaghoz.</span><span class="sxs-lookup"><span data-stu-id="f2cdd-110">The command passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="f2cdd-111">Ez a parancsmag eltávolítja a Web nevű végpont ACL-konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="f2cdd-111">That cmdlet removes the ACL configuration for the endpoint named Web.</span></span>
<span data-ttu-id="f2cdd-112">A parancs átadja az eredményt az **Update-AzureVM** parancsmagnak, amely frissíti a virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="f2cdd-112">The command passes the result to the **Update-AzureVM** cmdlet, which updates the virtual machine.</span></span>

## <span data-ttu-id="f2cdd-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f2cdd-113">PARAMETERS</span></span>

### <span data-ttu-id="f2cdd-114">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="f2cdd-114">-EndpointName</span></span>
<span data-ttu-id="f2cdd-115">Annak a végpontnak a neve, amelyből a parancsmag eltávolítja az ACL-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="f2cdd-115">Specifies the name of the endpoint from which this cmdlet removes the ACL configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2cdd-116">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="f2cdd-116">-InformationAction</span></span>
<span data-ttu-id="f2cdd-117">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="f2cdd-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="f2cdd-118">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="f2cdd-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f2cdd-119">Folytassa</span><span class="sxs-lookup"><span data-stu-id="f2cdd-119">Continue</span></span>
- <span data-ttu-id="f2cdd-120">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="f2cdd-120">Ignore</span></span>
- <span data-ttu-id="f2cdd-121">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="f2cdd-121">Inquire</span></span>
- <span data-ttu-id="f2cdd-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="f2cdd-122">SilentlyContinue</span></span>
- <span data-ttu-id="f2cdd-123">állj</span><span class="sxs-lookup"><span data-stu-id="f2cdd-123">Stop</span></span>
- <span data-ttu-id="f2cdd-124">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="f2cdd-124">Suspend</span></span>

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

### <span data-ttu-id="f2cdd-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="f2cdd-125">-InformationVariable</span></span>
<span data-ttu-id="f2cdd-126">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="f2cdd-126">Specifies an information variable.</span></span>

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

### <span data-ttu-id="f2cdd-127">-Profil</span><span class="sxs-lookup"><span data-stu-id="f2cdd-127">-Profile</span></span>
<span data-ttu-id="f2cdd-128">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="f2cdd-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f2cdd-129">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="f2cdd-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f2cdd-130">-VM</span><span class="sxs-lookup"><span data-stu-id="f2cdd-130">-VM</span></span>
<span data-ttu-id="f2cdd-131">Azt a virtuális gépet adja meg, amelyből ez a parancsmag eltávolítja az ACL-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="f2cdd-131">Specifies the virtual machine from which this cmdlet removes an ACL configuration.</span></span>

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

### <span data-ttu-id="f2cdd-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2cdd-132">CommonParameters</span></span>
<span data-ttu-id="f2cdd-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f2cdd-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2cdd-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2cdd-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2cdd-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f2cdd-135">INPUTS</span></span>

## <span data-ttu-id="f2cdd-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f2cdd-136">OUTPUTS</span></span>

## <span data-ttu-id="f2cdd-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f2cdd-137">NOTES</span></span>

## <span data-ttu-id="f2cdd-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f2cdd-138">RELATED LINKS</span></span>

[<span data-ttu-id="f2cdd-139">Get-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="f2cdd-139">Get-AzureAclConfig</span></span>](./Get-AzureAclConfig.md)

[<span data-ttu-id="f2cdd-140">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="f2cdd-140">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="f2cdd-141">Új – AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="f2cdd-141">New-AzureAclConfig</span></span>](./New-AzureAclConfig.md)

[<span data-ttu-id="f2cdd-142">Set-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="f2cdd-142">Set-AzureAclConfig</span></span>](./Set-AzureAclConfig.md)

[<span data-ttu-id="f2cdd-143">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="f2cdd-143">Update-AzureVM</span></span>](./Update-AzureVM.md)


