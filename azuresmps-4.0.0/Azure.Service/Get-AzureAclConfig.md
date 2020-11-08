---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 0A32348E-C38D-4555-8F7C-6515F4EE7F23
online version: ''
schema: 2.0.0
ms.openlocfilehash: cbc1c469d35f4cc281fa22252e7e81509be06761
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015673"
---
# <span data-ttu-id="c9eb8-101">Get-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="c9eb8-101">Get-AzureAclConfig</span></span>

## <span data-ttu-id="c9eb8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c9eb8-102">SYNOPSIS</span></span>
<span data-ttu-id="c9eb8-103">Az ACL konfigurációs objektum beolvasása egy Azure Virtual Machine-ből.</span><span class="sxs-lookup"><span data-stu-id="c9eb8-103">Gets the ACL configuration object from an Azure virtual machine.</span></span>

## <span data-ttu-id="c9eb8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c9eb8-104">SYNTAX</span></span>

```
Get-AzureAclConfig [[-EndpointName] <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="c9eb8-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c9eb8-105">DESCRIPTION</span></span>
<span data-ttu-id="c9eb8-106">A **Get-AzureAclConfig** parancsmag a hozzáférés-vezérlési lista (ACL) konfigurációs objektumát egy meglévő Azure virtuális gépről kapja.</span><span class="sxs-lookup"><span data-stu-id="c9eb8-106">The **Get-AzureAclConfig** cmdlet gets the access control list (ACL) configuration object from an existing Azure virtual machine.</span></span>

## <span data-ttu-id="c9eb8-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c9eb8-107">EXAMPLES</span></span>

### <span data-ttu-id="c9eb8-108">Példa 1: ACL-konfigurációs objektum beszerzése virtuális gép végpontjának</span><span class="sxs-lookup"><span data-stu-id="c9eb8-108">Example 1: Get an ACL configuration object for a virtual machine endpoint</span></span>
```
PS C:\> $Acl = Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Get-AzureAclConfig -EndpointName "Web"
```

<span data-ttu-id="c9eb8-109">Az első parancs a **Get-AzureVM** parancsmag használatával kapja meg a VirtualMachine07 nevű virtuális gépet a ContosoService nevű szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="c9eb8-109">The first command gets the virtual machine named VirtualMachine07 in the service named ContosoService by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="c9eb8-110">A parancs átadja az objektumot a **Get-AzureAclConfig** parancsmagnak a pipeline operátor használatával.</span><span class="sxs-lookup"><span data-stu-id="c9eb8-110">The command passes that object to the **Get-AzureAclConfig** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="c9eb8-111">Ez a parancsmag a Web nevű végpont ACL-konfigurációját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="c9eb8-111">That cmdlet gets the ACL configuration for the endpoint named Web.</span></span>
<span data-ttu-id="c9eb8-112">A parancs az ACL konfigurációs objektumát az $Acl változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="c9eb8-112">The command stores that ACL configuration object in the $Acl variable.</span></span>

## <span data-ttu-id="c9eb8-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c9eb8-113">PARAMETERS</span></span>

### <span data-ttu-id="c9eb8-114">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="c9eb8-114">-EndpointName</span></span>
<span data-ttu-id="c9eb8-115">Annak a végpontnak a nevét adja meg, amelynek a parancsmagja a hozzáférés-vezérlést kapja.</span><span class="sxs-lookup"><span data-stu-id="c9eb8-115">Specifies the name of the endpoint for which this cmdlet gets an ACL.</span></span>

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

### <span data-ttu-id="c9eb8-116">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="c9eb8-116">-InformationAction</span></span>
<span data-ttu-id="c9eb8-117">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="c9eb8-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="c9eb8-118">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="c9eb8-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c9eb8-119">Folytassa</span><span class="sxs-lookup"><span data-stu-id="c9eb8-119">Continue</span></span>
- <span data-ttu-id="c9eb8-120">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="c9eb8-120">Ignore</span></span>
- <span data-ttu-id="c9eb8-121">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="c9eb8-121">Inquire</span></span>
- <span data-ttu-id="c9eb8-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="c9eb8-122">SilentlyContinue</span></span>
- <span data-ttu-id="c9eb8-123">állj</span><span class="sxs-lookup"><span data-stu-id="c9eb8-123">Stop</span></span>
- <span data-ttu-id="c9eb8-124">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="c9eb8-124">Suspend</span></span>

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

### <span data-ttu-id="c9eb8-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="c9eb8-125">-InformationVariable</span></span>
<span data-ttu-id="c9eb8-126">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="c9eb8-126">Specifies an information variable.</span></span>

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

### <span data-ttu-id="c9eb8-127">-Profil</span><span class="sxs-lookup"><span data-stu-id="c9eb8-127">-Profile</span></span>
<span data-ttu-id="c9eb8-128">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="c9eb8-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c9eb8-129">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="c9eb8-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c9eb8-130">-VM</span><span class="sxs-lookup"><span data-stu-id="c9eb8-130">-VM</span></span>
<span data-ttu-id="c9eb8-131">Annak a virtuális gépnek az objektumát adja meg, amelyhez ez a parancsmag ACL-konfigurációt kap.</span><span class="sxs-lookup"><span data-stu-id="c9eb8-131">Specifies the virtual machine object for which this cmdlet gets ACL configuration.</span></span>

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

### <span data-ttu-id="c9eb8-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9eb8-132">CommonParameters</span></span>
<span data-ttu-id="c9eb8-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c9eb8-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9eb8-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9eb8-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9eb8-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c9eb8-135">INPUTS</span></span>

## <span data-ttu-id="c9eb8-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c9eb8-136">OUTPUTS</span></span>

## <span data-ttu-id="c9eb8-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c9eb8-137">NOTES</span></span>

## <span data-ttu-id="c9eb8-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c9eb8-138">RELATED LINKS</span></span>

[<span data-ttu-id="c9eb8-139">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="c9eb8-139">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="c9eb8-140">Új – AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="c9eb8-140">New-AzureAclConfig</span></span>](./New-AzureAclConfig.md)

[<span data-ttu-id="c9eb8-141">Remove-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="c9eb8-141">Remove-AzureAclConfig</span></span>](./Remove-AzureAclConfig.md)

[<span data-ttu-id="c9eb8-142">Set-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="c9eb8-142">Set-AzureAclConfig</span></span>](./Set-AzureAclConfig.md)


