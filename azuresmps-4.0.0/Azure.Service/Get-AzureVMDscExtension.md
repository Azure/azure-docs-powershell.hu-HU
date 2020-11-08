---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 9D6D1890-9442-45F1-A3AA-BB1DB5CB33D6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 462d40e463edf6894810ac6e00e39b9c7a9eabe1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016538"
---
# <span data-ttu-id="d947a-101">Get-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="d947a-101">Get-AzureVMDscExtension</span></span>

## <span data-ttu-id="d947a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d947a-102">SYNOPSIS</span></span>
<span data-ttu-id="d947a-103">A DSC bővítmény beállításait egy virtuális gépen kapja meg.</span><span class="sxs-lookup"><span data-stu-id="d947a-103">Gets the settings of the DSC extension on a virtual machine.</span></span>

## <span data-ttu-id="d947a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d947a-104">SYNTAX</span></span>

```
Get-AzureVMDscExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="d947a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d947a-105">DESCRIPTION</span></span>
<span data-ttu-id="d947a-106">A **Get-AzureVMDscExtension** PARANCSMAG a DSC bővítmény beállításait egy virtuális gépen kapja meg.</span><span class="sxs-lookup"><span data-stu-id="d947a-106">The **Get-AzureVMDscExtension** cmdlet gets the settings of the DSC extension on a virtual machine.</span></span>

## <span data-ttu-id="d947a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d947a-107">EXAMPLES</span></span>

### <span data-ttu-id="d947a-108">Példa 1: a DSC-bővítmény beállításának beszerzése virtuális gépen</span><span class="sxs-lookup"><span data-stu-id="d947a-108">Example 1: Get the setting of the DSC Extension on a virtual machine</span></span>
```
PS C:\> Get-AzureVMDscExtension -VM $VMModulesUrl
https://myaccount.blob.core.contoso.net/windows-powershell-dsc/MyConfiguration.ps1.zipConfigurationFunction : MyConfiguration.ps1\MyConfigurationProperties            : {ServerName}ExtensionName         : DSCPublisher             : Microsoft.PowershellVersion               : 1.*PrivateConfiguration  :PublicConfiguration   : {"ModulesUrl": "https://myaccount.blob.core.contoso.net/windows-powershell-dsc/MyConfiguration.ps1.zip","ConfigurationFunction": "MyConfiguration.ps1\\MyConfiguration","Properties": {"ServerName": "C:\\MyDirectory"}}ReferenceName         : DSCState                 : EnableRoleName              : my-vm
```

<span data-ttu-id="d947a-109">Ez a parancs egy virtuális gépen a DSC bővítmény beállításait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="d947a-109">This command gets the settings of the DSC Extension on a virtual machine.</span></span>

## <span data-ttu-id="d947a-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d947a-110">PARAMETERS</span></span>

### <span data-ttu-id="d947a-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="d947a-111">-InformationAction</span></span>
<span data-ttu-id="d947a-112">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="d947a-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="d947a-113">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="d947a-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d947a-114">Folytassa</span><span class="sxs-lookup"><span data-stu-id="d947a-114">Continue</span></span>
- <span data-ttu-id="d947a-115">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="d947a-115">Ignore</span></span>
- <span data-ttu-id="d947a-116">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="d947a-116">Inquire</span></span>
- <span data-ttu-id="d947a-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="d947a-117">SilentlyContinue</span></span>
- <span data-ttu-id="d947a-118">állj</span><span class="sxs-lookup"><span data-stu-id="d947a-118">Stop</span></span>
- <span data-ttu-id="d947a-119">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="d947a-119">Suspend</span></span>

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

### <span data-ttu-id="d947a-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="d947a-120">-InformationVariable</span></span>
<span data-ttu-id="d947a-121">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="d947a-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="d947a-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="d947a-122">-Profile</span></span>
<span data-ttu-id="d947a-123">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="d947a-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d947a-124">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="d947a-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d947a-125">-VM</span><span class="sxs-lookup"><span data-stu-id="d947a-125">-VM</span></span>
<span data-ttu-id="d947a-126">Az állandó virtuálisgép-objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="d947a-126">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="d947a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d947a-127">CommonParameters</span></span>
<span data-ttu-id="d947a-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d947a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d947a-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d947a-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d947a-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d947a-130">INPUTS</span></span>

## <span data-ttu-id="d947a-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d947a-131">OUTPUTS</span></span>

### <span data-ttu-id="d947a-132">Microsoft. WindowsAzure. Command. ServiceManagement. IaaS. Extensions. VirtualMachineDscExtensionContext</span><span class="sxs-lookup"><span data-stu-id="d947a-132">Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.VirtualMachineDscExtensionContext</span></span>

## <span data-ttu-id="d947a-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d947a-133">NOTES</span></span>

## <span data-ttu-id="d947a-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d947a-134">RELATED LINKS</span></span>

[<span data-ttu-id="d947a-135">Remove-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="d947a-135">Remove-AzureVMDscExtension</span></span>](./Remove-AzureVMDscExtension.md)

[<span data-ttu-id="d947a-136">Set-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="d947a-136">Set-AzureVMDscExtension</span></span>](./Set-AzureVMDscExtension.md)

[<span data-ttu-id="d947a-137">Get-AzureVMDscExtensionStatus</span><span class="sxs-lookup"><span data-stu-id="d947a-137">Get-AzureVMDscExtensionStatus</span></span>](./Get-AzureVMDscExtensionStatus.md)


