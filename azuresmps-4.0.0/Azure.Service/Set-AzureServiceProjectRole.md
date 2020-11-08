---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 5D093C10-F8B6-4F4A-ABD7-CC4D7AB7AFFA
online version: ''
schema: 2.0.0
ms.openlocfilehash: c78f53b95d18de600535368a1109b318294928c3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015952"
---
# <span data-ttu-id="71b09-101">Set-AzureServiceProjectRole</span><span class="sxs-lookup"><span data-stu-id="71b09-101">Set-AzureServiceProjectRole</span></span>

## <span data-ttu-id="71b09-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="71b09-102">SYNOPSIS</span></span>
<span data-ttu-id="71b09-103">Megadja a szerepkör példányainak vagy futásidejű verziójának számát.</span><span class="sxs-lookup"><span data-stu-id="71b09-103">Sets the number of instances or the runtime version of a role.</span></span>

## <span data-ttu-id="71b09-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="71b09-104">SYNTAX</span></span>

### <span data-ttu-id="71b09-105">Példányok</span><span class="sxs-lookup"><span data-stu-id="71b09-105">Instances</span></span>
```
Set-AzureServiceProjectRole [-RoleName <String>] -Instances <Int32> [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="71b09-106">Futtatókörnyezet</span><span class="sxs-lookup"><span data-stu-id="71b09-106">Runtime</span></span>
```
Set-AzureServiceProjectRole [-RoleName <String>] -Runtime <String> -Version <String> [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="71b09-107">VMSize</span><span class="sxs-lookup"><span data-stu-id="71b09-107">VMSize</span></span>
```
Set-AzureServiceProjectRole [-RoleName <String>] [-PassThru] -VMSize <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="71b09-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="71b09-108">DESCRIPTION</span></span>
<span data-ttu-id="71b09-109">Ez a témakör a Microsoft Azure PowerShell modul 0.8.10 verziójában található parancsmagot ismerteti.</span><span class="sxs-lookup"><span data-stu-id="71b09-109">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="71b09-110">A használt modul verziójának beszerzéséhez az Azure PowerShell konzolon írja be a következőt: `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="71b09-110">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="71b09-111">A **set-AzureServiceProjectRole** parancsmag a megadott szerepkörhöz tartozó szerepkör-példányok számát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="71b09-111">The **Set-AzureServiceProjectRole** cmdlet sets the number of role instances for the specified role.</span></span>

## <span data-ttu-id="71b09-112">Példák</span><span class="sxs-lookup"><span data-stu-id="71b09-112">EXAMPLES</span></span>

### <span data-ttu-id="71b09-113">Példa 1: webes szerepkör példányainak beállítása</span><span class="sxs-lookup"><span data-stu-id="71b09-113">Example 1: Set instances for a web role</span></span>
```
PS C:\> Set-AzureServiceProjectRole "MyWebRole" 2
```

<span data-ttu-id="71b09-114">A MyWebRole1 nevű webszerepkör példányainak számát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="71b09-114">Sets the number of instances for the web role named MyWebRole1 to 2.</span></span>

### <span data-ttu-id="71b09-115">2. példa: a munkatársi szerepkör példányainak beállítása</span><span class="sxs-lookup"><span data-stu-id="71b09-115">Example 2: Set instances for a worker role</span></span>
```
PS C:\> Set-AzureServiceProjectRole "MyWorkerRole1" 2
```

<span data-ttu-id="71b09-116">A WorkerRole1 és a 2 nevű munkatársi szerepkör szerepkör-példányának számát állítja be.</span><span class="sxs-lookup"><span data-stu-id="71b09-116">Sets the role instance count for the worker role named WorkerRole1 to 2.</span></span>

### <span data-ttu-id="71b09-117">3. példa: egy szerepkör-szolgáltatás futásidejű verziójának beállítása</span><span class="sxs-lookup"><span data-stu-id="71b09-117">Example 3: Set the runtime version for a role service</span></span>
```
PS C:\> Set-AzureServiceProjectRole "MyRole1" node 0.6.20
```

<span data-ttu-id="71b09-118">A 0.6.20 szerepkör-MyRole1 a node.exe futtatókörnyezet-verziót állítja be.</span><span class="sxs-lookup"><span data-stu-id="71b09-118">Sets the node.exe runtime version for role MyRole1 to 0.6.20.</span></span>

## <span data-ttu-id="71b09-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="71b09-119">PARAMETERS</span></span>

### <span data-ttu-id="71b09-120">-Példányok</span><span class="sxs-lookup"><span data-stu-id="71b09-120">-Instances</span></span>
<span data-ttu-id="71b09-121">A megadott webes vagy munkatársi szerepkörhöz tartozó szerepkör-példányok számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="71b09-121">Specifies the number of role instances for the specified web or worker role.</span></span>

```yaml
Type: Int32
Parameter Sets: Instances
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71b09-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="71b09-122">-PassThru</span></span>
<span data-ttu-id="71b09-123">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="71b09-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="71b09-124">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="71b09-124">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71b09-125">-Profil</span><span class="sxs-lookup"><span data-stu-id="71b09-125">-Profile</span></span>
<span data-ttu-id="71b09-126">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="71b09-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="71b09-127">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="71b09-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="71b09-128">-RoleName</span><span class="sxs-lookup"><span data-stu-id="71b09-128">-RoleName</span></span>
<span data-ttu-id="71b09-129">A módosítani kívánt webes vagy munkatársi szerepkör nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="71b09-129">Specifies the name of the web or worker role to be changed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71b09-130">-Futtatókörnyezet</span><span class="sxs-lookup"><span data-stu-id="71b09-130">-Runtime</span></span>
<span data-ttu-id="71b09-131">A megadott szerepkörhöz hozzáadni kívánt futtatókörnyezetet adja meg.</span><span class="sxs-lookup"><span data-stu-id="71b09-131">Specifies the runtime to add to the specified role.</span></span>

```yaml
Type: String
Parameter Sets: Runtime
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71b09-132">-Verzió</span><span class="sxs-lookup"><span data-stu-id="71b09-132">-Version</span></span>
<span data-ttu-id="71b09-133">Itt adhatja meg a szerepkörhöz hozzáadni kívánt futásidejű verziót.</span><span class="sxs-lookup"><span data-stu-id="71b09-133">Specifies the version of the runtime to add to the role.</span></span>

```yaml
Type: String
Parameter Sets: Runtime
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71b09-134">-VMSize</span><span class="sxs-lookup"><span data-stu-id="71b09-134">-VMSize</span></span>
<span data-ttu-id="71b09-135">A szerepkör virtuális gép méretét adja meg.</span><span class="sxs-lookup"><span data-stu-id="71b09-135">Specifies the virtual machine size of the role.</span></span>

```yaml
Type: String
Parameter Sets: VMSize
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71b09-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71b09-136">CommonParameters</span></span>
<span data-ttu-id="71b09-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="71b09-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71b09-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71b09-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71b09-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="71b09-139">INPUTS</span></span>

###  
<span data-ttu-id="71b09-140">A virtuális gép méretét adja meg.</span><span class="sxs-lookup"><span data-stu-id="71b09-140">Specifies the size of the virtual machine.</span></span>

## <span data-ttu-id="71b09-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="71b09-141">OUTPUTS</span></span>

## <span data-ttu-id="71b09-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="71b09-142">NOTES</span></span>

## <span data-ttu-id="71b09-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="71b09-143">RELATED LINKS</span></span>

[<span data-ttu-id="71b09-144">Set-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="71b09-144">Set-AzureServiceProject</span></span>](./Set-AzureServiceProject.md)


